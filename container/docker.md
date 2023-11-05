# Beginner Study Guide
Time: 28 - 30 hours

# Session 1 (4 hours)
- [ ] Read walkthrough on Container Security (Datadog Security Labs)
	- [ ] [Container security fundamentals: Exploring containers as processes](https://securitylabs.datadoghq.com/articles/container-security-fundamentals-part-1/)
	- [ ] [Container security fundamentals part 2: Isolation & namespaces]()
	- [ ] [Container security fundamentals part 3: Capabilities](https://securitylabs.datadoghq.com/articles/container-security-fundamentals-part-3/)
	- [ ] [Container security fundamentals part 4: Cgroups](https://securitylabs.datadoghq.com/articles/container-security-fundamentals-part-4/)
	- [ ] [Container security fundamentals part 5: AppArmor and SELinux](https://securitylabs.datadoghq.com/articles/container-security-fundamentals-part-5/)
	- [ ] [Container security fundamentals part 6: seccomp](https://securitylabs.datadoghq.com/articles/container-security-fundamentals-part-6/)
- [ ] Watch `The Container Security Checklist`
	- [ ] https://www.youtube.com/watch?v=uTl1ouuC3IA&ab_channel=CNCF%5BCloudNativeComputingFoundation%5D
- [ ] Container Escape (Process Escape)
	- [ ] Watch `A Compendium of Container Escapes` from Brandon Edwards & Nick Freeman (BHUSA 2019)
		- [ ] https://www.youtube.com/watch?v=BQlqita2D2s&ab_channel=BlackHat (43 mins)
		- [ ] https://i.blackhat.com/USA-19/Thursday/us-19-Edwards-Compendium-Of-Container-Escapes-up.pdf
		- [ ] https://web.archive.org/web/20210425171222/https://capsule8.com/blog/practical-container-escape-exercise/
	- [ ] Watch `Kubernetes Privilege Escalation: Container Escape == Cluster Admin?` (BHUSA 2022)
		- [ ] https://www.youtube.com/watch?v=oc1tq_r6VNM
	- [ ] Read `Understanding Docker container escapes` from Trail of Bits
		- [ ] https://blog.trailofbits.com/2019/07/19/understanding-docker-container-escapes/
	- [ ] Read `The Strange Case of How We Escaped the Docker Default Container`
		- [ ] https://www.cyberark.com/resources/threat-research-blog/the-strange-case-of-how-we-escaped-the-docker-default-container
	- [ ] Watch `Container Escape In 2021` by Li Qiang (HITB2021)
		- [ ] https://www.youtube.com/watch?v=WBC7hhgMvQQ&ab_channel=HackInTheBoxSecurityConference
- [ ] Note down the reference for Docker Privilege Escalation
	- [ ] https://book.hacktricks.xyz/linux-hardening/privilege-escalation/docker-security/docker-breakout-privilege-escalation
# Session 2 (4 hours)
- Setting up Linux VM environment for Docker
- Continue with Container Escape Readings if not completed
- Get familiar with Docker cli commands
	- https://docs.docker.com/engine/security/
	- https://docs.docker.com/engine/reference/run/#runtime-privilege-and-linux-capabilities
	- https://docs.docker.com/engine/security/protect-access/
- https://gist.github.com/FrankSpierings/5c79523ba693aaa38bc963083f48456c
# Session 3 (4 hours)
- Solve some Docker rootme exercises
	- https://www.root-me.org/fr/Challenges/App-Script/Docker-Talk-through-me
	- https://www.root-me.org/fr/Challenges/App-Script/Docker-Sys-Admin-s-Docker
	- https://www.root-me.org/fr/Challenges/Forensic/Docker-layers
	- https://www.root-me.org/fr/Challenges/App-Script/Docker-I-am-groot
	- https://www.root-me.org/fr/Challenges/Forensic/Supply-chain-attack-Docker
# Session 4 (4 hours)
- Fun with privileged container breakout
	- https://raesene.github.io/blog/2023/08/06/fun-with-privileged-container-breakout/
# Session 5 (4 hours)

# Session 6 (4 hours)
- THM Room: Hamlet
	- https://tryhackme.com/room/hamlet
	- https://www.youtube.com/watch?v=KHFAKETn0GY&ab_channel=I.TSecurityLabs (3o mins)
# Session 7 (4 hours)
- Read more advanced techniques
	- https://starlabs.sg/blog/2023/07-a-new-method-for-container-escape-using-file-based-dirtycred/
