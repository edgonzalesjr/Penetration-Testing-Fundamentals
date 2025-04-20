## Objective
To gain practical, hands-on experience in the core stages of penetration testing - reconnaissance, enumeration, exploitation, and privilege escalation - while developing analytical thinking and ethical hacking methodologies aligned with the responsibilities of a Security Analyst.

### Skills Learned
- Reconnaissance & Enumeration
  - Identified open ports and services (TCP scanning)
  - Discovered hidden web directories and user accounts
  - Interpreted scan outputs to assess system exposure
- Exploitation Techniques
  - Conducted brute-force attacks on directories and login credentials
  - Gained unauthorized access to systems ethically for assessment purposes
- Privilege Escalation
  - Analyzed local vulnerabilities to elevate privileges
  - Understood misconfigurations and poor permission controls
- Analytical Thinking
  - Interpreted tool outputs to form hypotheses about potential exploits
  - Evaluated each discovery for its significance in the attack chain
- Ethical Practice
  - Recognized the ethical implications of offensive tools
  - Practiced responsible hacking within a safe, legal lab environment

### Tools Used
- Kali Linux: Penetration testing tool to perform attacks on a vulnerable machine.
- VMWare Workstation: Isolated environment for testing and simulation.
- Vulnerable VM machine: boot2root virtual machine designed to practice remote exploitation and privilege escalation techniques.
- Nmap:	Service detection, port scanning, reconnaissance.
- Gobuster:	Web directory brute-forcing.
- enum4linux:	User enumeration from Samba shares.
- Hydra:	Password brute-forcing for authentication services.
- LinPeas	Privilege: escalation enumeration and vulnerability discovery.

## Practical Exercises

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/01_Run a ping sweep on the network.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Run a ping sweep on the network. The IP address of the target machine has been identified.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/02_This scan identifies open ports on the target machine.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>This scan identifies open ports on the target machine, detects running services and their versions, and executes default scripts to gather additional information or uncover potential issues.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/03_The scan shows that the host 192.168.10.3 is online.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>The scan shows that the host 192.168.10.3 is online with several open services:
   - SSH (port 22): Running OpenSSH 7.2p2 on Ubuntu.
   - HTTP (port 80): Apache 2.4.18 web server.
   - Samba (ports 139, 445): Samba file sharing enabled, version 4.3.11.
   - AJP (port 8009): Apache JServ Protocol active.
   - Tomcat (port 8080): Apache Tomcat 9.0.7 web server interface.
</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/04_Interact with the running website_1.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/04_Interact with the running website_2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Interact with the running website, then view the page source to inspect the HTML code.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/05_The comment suggests we try navigating to the dev folder.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>The comment suggests we try navigating to the /dev folder. We've also identified that the server is running Apache/2.4.18 (Ubuntu).</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/06_As the available paths on the web server are unknown_1.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/06_As the available paths on the web server are unknown_2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/06_As the available paths on the web server are unknown_3.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/06_As the available paths on the web server are unknown_4.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>As the available paths on the web server are unknown, we used a tool to enumerate potential directories. This revealed a /development folder, which contains a directory listing with several text files.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/07_To identify possible users on the target machine_1.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/07_To identify possible users on the target machine_2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>To identify possible users on the target machine, we decided to explore the SMB service using enum4linux. This revealed two Linux user accounts.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/08_Since the note suggests that user jan.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Since the note suggests that user 'jan' has a weak password, we’ll use Hydra to attempt a brute-force login.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/09_Hydra successfully brute-forced the SSH login.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Hydra successfully brute-forced the SSH login with the username 'jan' and the password 'armando', granting access to the system.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/10_We now have the credentials to log in.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>We now have the credentials to log in to the machine via SSH. Let’s initiate the SSH connection.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/11_We’ll perform some basic tasks_1.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/11_We’ll perform some basic tasks_2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/11_We’ll perform some basic tasks_3.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>We’ll perform some basic tasks on the machine.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/12_We’ll transfer and run linpeas_1.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/12_We’ll transfer and run linpeas_2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/12_We’ll transfer and run linpeas_3.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/12_We’ll transfer and run linpeas_4.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>We’ll transfer and run linpeas.sh on the remote machine for privilege escalation, which revealed private SSH keys.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/13_We’ll attempt to read_1.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/13_We’ll attempt to read_2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>We’ll attempt to read Kay’s private SSH key and save a copy for later use.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/14_We’ll convert the _1.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/14_We’ll convert the _2.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>We’ll convert the private key to a John-compatible format, then use a wordlist with John the Ripper to crack the passphrase. The password for kay_id_rsa was successfully recovered.</b>
<br/>

<p align="center">
<img src="https://github.com/edgonzalesjr/Penetration-Testing-Fundamentals/blob/main/images/15_Using the saved.png" height="90%" width="90%" alt="Device Specification"/>
<br/>
<b>Using the saved private key and the recovered passphrase, we can SSH into the machine and have successfully gained root access.</b>
<br/>

## Outcome
- Practical Understanding of the Attack Lifecycle: Gained end-to-end experience with a simulated attack, from discovery to exploitation and privilege escalation.
- Bridged Theory and Real-World Practice: Reinforced foundational concepts with hands-on implementation, preparing for complex red team/blue team operations.
- Enhanced Threat Awareness: Improved recognition of common misconfigurations in SSH, Samba, and Linux privilege escalation vectors.
- Security Analyst Readiness: Developed a mindset for identifying vulnerabilities and anticipating attacker tactics—critical for threat detection, incident response, and vulnerability management in a Security Analyst role.

## Acknowledgements
This project combines ideas and methods from various sources, such as the Basic Penetration Testing by John Hammond, Josiah Pierce vulnerable VM and my IT experience. These resources provided the fundamental information and techniques, which were then modified in light of practical uses. 
 - [John Hammond](https://www.youtube.com/watch?v=xl2Xx5YOKcI&t=57s)
 - [TryHackMe Basic Pentesting](https://tryhackme.com/room/basicpentestingjt/)
 - [Josiah Pierce](https://www.vulnhub.com/series/basic-pentesting,143/)
 - [Kali Linux](https://www.kali.org/) 
 - [VMWare Workstation](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)

## Disclaimer
The sole goals of the projects and activities here are for education and ethical cybersecurity research. All work was conducted in controlled environments, such as paid cloud spaces, private labs, and online cybersecurity education platforms. Online learning and cloud tasks adhered closely to all usage guidelines. Never use these projects for improper or unlawful purposes. It is always prohibited to break into any computer system or network. Any misuse of the provided information or code is not the responsibility of the author or authors.
 

