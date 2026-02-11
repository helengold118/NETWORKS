# 🔐 Network Security Using Virtual Local Area Networks (VLANs)

## 📄 Abstract

This hypothetical document presents an overview of how **Virtual Local Area Networks (VLANs)** can be used as an effective network security mechanism. It outlines objectives, methodology, and structured sections to demonstrate how VLANs enhance segmentation, reduce attack surfaces, and improve overall network performance and security.

---

## 📚 Table of Contents

1. 🧭 Introduction to Network Security
2. 🌐 Overview of VLAN Technology
3. 🎯 Objectives of Implementing VLANs
4. 🛠️ Methodology
5. 🔒 VLANs as a Network Security Control
6. ⚠️ Threats Mitigated by VLAN Implementation
7. 🧪 Hypothetical Network Design Scenario
8. 📈 Benefits and Limitations
9. ✅ Conclusionn

---

## 🧭 1. Introduction to Network Security

Network security involves the protection of network infrastructure, devices, and data from unauthorized access, misuse, or attacks. As modern networks grow in size and complexity, segmentation becomes critical for maintaining security and efficiency.

---

## 🌐 2. Overview of VLAN Technology

A **Virtual Local Area Network (VLAN)** is a logical grouping of network devices configured on a switch, independent of physical location. VLANs allow administrators to segment networks based on function, department, or security level.

🔹 Key Characteristics:

* Logical segmentation
* Reduced broadcast domains
* Improved traffic control

---

## 🎯 3. Objectives of Implementing VLANs

The primary objectives of using VLANs in network security include:

* 🔐 **Enhancing Security** – Isolating sensitive systems from general users
* 🚦 **Traffic Control** – Limiting broadcast traffic
* 🧩 **Network Segmentation** – Separating departments or roles
* ⚙️ **Improved Performance** – Reducing congestion
* 🛡️ **Attack Surface Reduction** – Containing potential threats

---

## 🛠️ 4. Methodology

The methodology adopted in this hypothetical implementation includes the following steps:

1. 📝 **Network Assessment** – Identify devices, users, and security requirements
2. 🧱 **VLAN Design** – Assign VLAN IDs based on departments or trust levels
3. 🔌 **Switch Configuration** – Configure access and trunk ports
4. 🔄 **Inter-VLAN Routing** – Enable controlled communication using Layer 3 devices
5. 🔍 **Testing & Validation** – Verify segmentation and access control
6. 📊 **Monitoring** – Continuously observe traffic and logs

---

## 🔒 5. VLANs as a Network Security Control

VLANs act as a first line of defense by:

* 🚫 Preventing unauthorized lateral movement
* 🧭 Enforcing logical separation
* 🔑 Supporting access control policies

When combined with ACLs and firewalls, VLANs significantly strengthen network security.

---

## ⚠️ 6. Threats Mitigated by VLAN Implementation

VLANs help mitigate several common network threats:

* 🐛 ARP Spoofing
* 📡 Broadcast Storms
* 🕵️ Unauthorized Network Access
* 🔄 Internal Reconnaissance

---

## 🧪 7. Hypothetical Network Design Scenario

In a hypothetical o<img width="1327" height="780" alt="router config" src="https://github.com/user-attachments/assets/6ea614f5-18cf-40ae-9fee-eb6a751304a0" />
rganization:

* 🧑‍💼 VLAN 10 – Management
* 💻 VLAN 20 – IT Department
* 🧾 VLAN 30 – Finance
* 🌐 VLAN 40 – Guest Network

Each VLAN is isolated, with restricted inter-VLAN communication enforced via routing and ACLs.

---

## 📈 8. Benefits and Limitations
<img width="787" height="763" alt="port security 2" src="https://github.com/user-attachments/assets/6fe55e0c-f980-4377-9514-7b982fb93bf1" />



### ✅ Benefits

* Improved security posture 🔐
* Better network organization 🗂️
* Scalability 📊

### ❌ Limitations

* Misconfiguration risks ⚠️
* Requires skilled administration 👨‍💻
* VLAN hopping if poorly secured 🕳️

---

## ✅ 9. ConclusionJJ

VLANs are a powerful and cost-effective tool for enhancing network security. When properly designed and implemented, they provide strong segmentation, improved performance, and a solid foundation for layered network defense strategies.

---





🛡️<h1><strong> Metasploit Penetration Test on Metasploitable 2 (From Linux Attacker Machine)</strong></h1>
📌 **Project Overview**

This repository documents a practical penetration testing lab performed using the Metasploit Framework against the intentionally vulnerable Metasploitable 2 virtual machine. The attack was executed from a Linux-based penetration testing environment to demonstrate real-world offensive security techniques including reconnaissance, vulnerability scanning, exploitation, and post-exploitation.

This project is intended strictly for educational and ethical hacking purposes within a controlled lab environment.

🎯 **Objectives**

Understand real-world penetration testing methodology.

Perform network reconnaissance and enumeration.

Identify vulnerable services on Metasploitable 2.

Exploit discovered vulnerabilities using Metasploit.

Gain system access and perform post-exploitation activities.

Document findings in a structured methodology.

🧰<h1><strong> Tools and Technologies</strong></h1>

Linux (Kali Linux / Ubuntu penetration testing setup)

Metasploit Framework

Nmap

Metasploitable 2 VM

VirtualBox / VMware

Terminal (CLI)

🖥️ Lab Setup
Attacker Machine

OS: Linux (Kali Linux recommended)

IP Address: 192.168.x.x

Target Machine

OS: Metasploitable 2

IP Address: 192.168.x.x

Both machines were configured on the same virtual network (Host-Only or NAT Network).

🔎 Step 1 — Network Discovery

Identify active hosts on the network.

nmap -sn 192.168.56.0/24


Result:

Target system identified as Metasploitable 2.

🔍 Step 2 — Port Scanning and Service Enumeration

Perform a detailed scan to identify open ports and services.

nmap -sV 192.168.56.**
<img width="966" height="891" alt="pentest 1" src="https://github.com/user-attachments/assets/c9e65e6c-eee4-42b0-9a92-b0858c93f131" />

Discovered Services:

FTP (vsftpd)

SSH

Telnet

HTTP (Apache)

MySQL

Samba

IRC

UnrealIRCd

PostgreSQL

Metasploitable 2 intentionally reminded us how dangerous exposed services can be without proper hardening.

💣 Step 3 — Launching Metasploit
<img width="967" height="932" alt="pentest 2" src="https://github.com/user-attachments/assets/a95a5580-0abd-4c95-98a6-abe210c2511f" />

Start Metasploit Framework:

msfconsole

🎯 Step 4 — Vulnerability Search

Search for known exploits based on discovered services.
<img width="956" height="881" alt="pentest 3" src="https://github.com/user-attachments/assets/12d1eb2f-1e29-4960-87bb-378a6055d2f2" />

Example:

search vsftpd

🚀 Step 5 — Exploitation (Example: UnrealIRCd Backdoor)

Select exploit:

use exploit/unix/irc/unreal_ircd_3281_backdoor
<img width="952" height="703" alt="pentest 4" src="https://github.com/user-attachments/assets/3e63c619-442e-41af-8f23-59418f9bb190" />


Configure target:

set RHOSTS 192.168.**.*



Execute:

run

Result:

Successful shell access obtained.

🔓 Step 6 — Privilege Verification

Check system access:
uname -a
<img width="980" height="912" alt="pentest 5" src="https://github.com/user-attachments/assets/620faba5-21df-46c7-a6e3-c2881b92ae4d" />


Metasploitable often provides root-level access due to intentional misconfiguration.

⚙️ Step 7 — Post Exploitation

Example activities:

System enumeration

Checking user accounts

Viewing sensitive files

Commands:

cat /etc/passwd
ls
id

📊 Key Findings

Multiple outdated services exposed.

Weak or no authentication on some services.

Backdoor vulnerabilities present.

Lack of network segmentation.

🔐 Security Recommendations

Disable unused services.

Implement strict firewall rules.

Patch vulnerable applications.

Apply network segmentation using ACLs.

Enforce strong authentication policies.

🧠 Lessons Learned

Enumeration is the most critical phase in penetration testing.

Misconfigured services dramatically increase attack surface.

Automated frameworks like Metasploit accelerate exploitation.

Defense-in-depth is essential for enterprise security.

⚠️ Ethical Disclaimer

This project was performed in a controlled lab environment using intentionally vulnerable systems. Do not attempt these techniques on systems without proper authorization.

⭐ Skills Demonstrated

Network reconnaissance

Vulnerability assessment

Exploit execution

Linux command-line usage

Metasploit framework

Ethical hacking methodology.




 <h1><strong>Standard ACL and Wildcard Mask Configuration — Practical Cisco Networking Lab</strong></h1>
📌 Project Overview

This repository documents the configuration and implementation of Standard Access Control Lists (ACLs) using wildcard masks on Cisco network devices. The goal of this lab is to demonstrate how network administrators control traffic flow by filtering packets based on source IP addresses while applying security best practices.

Standard ACLs are widely used in enterprise environments to enforce basic traffic filtering, improve network segmentation, and enhance overall security posture.

🎯 Objectives

Understand Standard ACL functionality.

Learn Cisco ACL numbering conventions.

Configure Standard ACLs using wildcard masks.

Apply ACLs to network interfaces.

Verify and troubleshoot ACL behavior.

Demonstrate real-world network access control scenarios.

🧰 Technologies and Tools

Cisco Router / Cisco Packet Tracer / GNS3

Cisco IOS CLI

Networking fundamentals (IP addressing, subnetting)

📚 Concept Overview
✅ What is a Standard ACL?

A Standard Access Control List filters traffic based only on:

Source IP address

Unlike extended ACLs, standard ACLs cannot filter based on:

Destination IP

Protocol type

Port numbers

🔢 Standard ACL Number Range

Standard ACLs use the following numbering:

1 – 99 (original range)

1300 – 1999 (expanded range)

Example:

access-list 10 permit 192.168.1.0 0.0.0.255

🌐 Wildcard Mask Explained

A wildcard mask determines which bits of an IP address must match.

It is essentially the inverse of a subnet mask.

Key Rules:

0 = Must match exactly.

1 = Ignore (any value allowed).

Example Comparison
Subnet Mask	Wildcard Mask
255.255.255.0	0.0.0.255
255.255.0.0	0.0.255.255
255.0.0.0	0.255.255.255

🚀 Configuration Steps
Step 1 — Enter Global Configuration Mode
enable
configure terminal

<img width="1756" height="1030" alt="ACL 1" src="https://github.com/user-attachments/assets/044e24c8-f48a-4871-a52e-d26a0eab611a" />

Step 2 — Create Standard ACL
access-list 10 permit 192.168.1.0 0.0.0.255
access-list 10 deny any

<img width="1531" height="937" alt="new ACL" src="https://github.com/user-attachments/assets/be64ae72-8f12-40f2-b7e0-807a8ecb67c7" />


Explanation:

Permit traffic from 192.168.1.0/24

Deny all other sources (implicit deny also exists).

Step 3 — Apply ACL to Interface

Standard ACL best practice:

👉 Place close to destination.

interface GigabitEthernet0/1
ip access-group 10 in

🔎 Verification

Check ACL configuration:

show access-lists

<img width="1108" height="947" alt="ACL 2" src="https://github.com/user-attachments/assets/ad2d007a-b262-48fb-8f84-234f6ba02789" />

Check interface application:

show running-config

📊 Expected Results

✅ Devices from 192.168.1.0 network allowed.
❌ All other traffic blocked.

⚠️ Important Notes

ACLs are processed top-down.

First matching rule applies.

Implicit deny exists at the end of every ACL.

Rule order is critical.

🔐 Security Best Practices

Use descriptive naming (named ACLs when possible).

Document wildcard mask logic.

Apply least privilege principle.

Avoid overly permissive rules.

Regularly audit ACL entries.

🧠 Real-World Applications

Enterprise network segmentation.

Restricting management access.

Protecting sensitive servers.

Basic firewall filtering.

Controlling inter-VLAN communication.

🎓 Skills Demonstrated

Cisco ACL configuration

Wildcard mask calculation

Network traffic filtering

Security policy implementation

Troubleshooting ACL behavior

⚠️ Ethical Notice

This lab is for educational purposes within controlled environments only.
