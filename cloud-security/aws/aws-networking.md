# Challenges
- How to enable secure communication between Internet (public IP) and VPC (private subnet)? 
  [[AWS Networking#How do you communicate between Internet and private Subnet?]]
- How to enable secure communication between two VPCs? 
  [[AWS Networking#How to enable secure communication between two VPCs?]]
- How to connect between AWS resources without going through public Internet? 
  [[AWS Networking#How to connect between AWS resources without going through public Internet?]]

# How to enable secure communication between two VPCs?
- Communication between VPCs through internet
- VPC Peering [[AWS Networking#VPC Peering]]

# How do you communicate between Internet and private Subnet?
- Use Internet Gateway
- Use Network Address Translation (NAT)

# How to connect between AWS resources without going through public Internet?
- Interface VPC endpoints allow private subnets to communicate with AWS public resources such as S3, Amazon SQS, Kinesis and API Gateway.

# Internet Gateway (IGW)
- If you want two-way communication between the Internet and private Subnet, we can use IGW.
- Configure the route table in NACL to route traffic to the IGW.

# Network Address Translation (NAT)
- NAT will translate the IP addresses of the private subnet into public subnet IP address.
	- Hence NAT is placed at public subnet instead of private subnet.
- One of the uses of NAT is to allow traffic from private subnet to communicate with internet-bound. 
- At the same time, NAT does not allow internet traffic to move into the private subnet.
	- This communication will be one-way (from resources in private subnet to internet)
- NAT is created at subnet level whereas Internet Gateway is created at VPC level.
- NAT will communicate with the IGW to internet.

# Route Tables (RT)
- Created for each VPC subnets
- Each route in RT must be given Destination (CIDR) and Target (e.g. local, IGW, etc.)
- Allows us to route traffic to different network components such as local network (private subnet), Internet Gateway (IGW), NAT, Transit Gateway (TGW), etc.

# Access Control
- NACL is stateless while SG is stateful.

## Network Access Control List (NACL)
- NACL is stateless -> This means that if you have a rule to allow incoming traffic, it doesn't explicitly allow that outgoing traffic (response) to the endpoint is allowed.
- So we need to explicitly allow incoming and outgoing traffic if we want to send a request and receive a response.
- Parts of the rule
	- Inbound / Outbound
	- Rule Number
	- Type
	- Protocol
	- Port range
	- Source / Destination
	- Allow or Deny
- The rules of NACL are evaluated from lowest level to highest level. If the lower level rule is evaluated and matched, the traffic will be allowed or denied.

## Security Groups (SG)
- SG is stateful -> This means if you allow incoming traffic in, it will implicitly allow traffic out.
- This applies to Elastic Network Interface (ENI) of EC2 instances.
- SG doesn't allow you to deny traffic into the ENI. To deny traffic, we need to use NACL.

# VPC Peering
- We can use VPC peering to route traffic between two VPCs without going through Internet (public IP).
