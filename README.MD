# Honeypot Assignment

**Time spent:** **5** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?
To deploy the project, I used Google Cloud Provider (GCP) and the Compute Engine module. This allowed me to set up MHN and establish the necessary firewall rules:

1: allow TCP 80 ingress connection for access the MHN dashboard
2: allow TCP 3000 ingress connection for access to HoneyMap Feature From Anywhere
3: allow TCP 10000 ingress connection for accesss to HPFeeds From Anywhere 

<img src="mhn-admin.gif">

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

<img src="dionaea-honeypot.gif">

## Notes

Describe any challenges encountered while doing the assignment.

Everything went smoothly



