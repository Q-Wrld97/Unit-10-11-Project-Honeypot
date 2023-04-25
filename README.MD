# Honeypot Assignment

**Time spent:** **5** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?
To deploy the project, I used Google Cloud Provider (GCP) and the Compute Engine module. This allowed me to set up MHN and establish the necessary firewall rules:

1: allow TCP 80 ingress connection for access the MHN dashboard
2: allow TCP 3000 ingress connection for access to HoneyMap Feature From Anywhere
3: allow TCP 10000 ingress connection for accesss to HPFeeds From Anywhere 

<img src="M0.png">
<img src="M1.png">
<img src="M1_P2.png">
<img src="M2.png">


### Dionaea Honeypot Deployment (Required)

**Summary:** Dionaea is a honeypot designed to trap malware and exploit vulnerabilities in services offered on a network. The primary goal of Dionaea is to obtain a copy of the attacking malware and log its activity via HPFeeds. Dionaea was deployed on an Ubuntu-minimal-1804-lts virtual machine (VM) with the following firewall rule:

Allow all TCP and UDP ports (wide open)
The most common ports of attack that Dionaea emulates include:

blackhole
epmap
ftp
http
memcache
mirror
mqtt
mssql
mysql
pptp
sip
smb
tftp
upnp

Dionaea achieves its functionality by embedding Python using the Flask framework and employing libemu to detect shellcode.
<img src="M3.png">
<img src="M4.png">
<img src="M5.png">
<img src="M5_P2.png">
## Notes

Describe any challenges encountered while doing the assignment.

Everything went smoothly

##Conclusion
By setting up a honeynet with MHN-Admin and deploying a Dionaea honeypot, we have demonstrated the potential risks and vulnerabilities that exist in the current state of Internet security. This exercise highlights the importance of allocating more resources to the IT security team to proactively address these threats and protect the company's valuable assets.


