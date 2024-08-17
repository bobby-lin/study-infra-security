# DR Storage
| Service            | AZ Resilient                               | Regional Resilient                                      |
| ------------------ | ------------------------------------------ | ------------------------------------------------------- |
| EC2 Instance Store | No                                         | No                                                      |
| EBS                | Yes if volume snapshot to single region S3 | Yes if volume snapshot to multi region S3               |
| S3                 | Yes                                        | Yes if cross region replication (crr) of bucket is used |
| EFS                | Yes                                        | No                                                      |

# DR Compute
| Service              | AZ Resilient | Regional Resilient |
| -------------------- | ------------ | ------------------ |
| EC2 Instance         | No           | No                 |
| ASG (Instance)       | Yes          | No                 |
| ECS - EC2 mode       | No           | No                 |
| ECS - Fargate mode   | Yes          | No                 |
| Private Lambda (VPC) | Yes          | No                 |
| Public Lambda        | Yes          | No                 |

# DR Databae
| Service                          | AZ Resilient                                  | Regional Resilient |
| -------------------------------- | --------------------------------------------- | ------------------ |
| DB (hosted in EC2)               | No                                            | No                 |
| RDS (pri + sec)                  | Yes if multi-AZ are not down at the same time | No                 |
| RDS (cross region read replicas) | Yes                                           | Yes                |
| DynamoDB                         | Yes                                           | No                 |
| DynamoDB (Global Table)          | Yes                                           | Yes                |
| Aurora                           | Yes                                           | No                 |
| Aurora (Global Database)         | Yes                                           | Yes                |

# DR Networking
| Service                      | AZ Resilient | Regional Resilient |
| ---------------------------- | ------------ | ------------------ |
| VPC                          | Yes          | No                 |
| IGW                          | Yes          | No                 |
| VPC Router                   | Yes          | No                 |
| NATGW (Single)               | No           | No                 |
| NATGW (Multi-AZ)             | Yes          | No                 |
| R53                          | Yes          | Yes                |
| ENI (attach to Subnet in AZ) | No           | No                 |
| ELB                          | Yes          | No                 |
| Interface Endpoint           | No           | No                 |
