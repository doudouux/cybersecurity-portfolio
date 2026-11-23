---
layout: home
title: Home
---

## 1. About me

I am a first-year Master's student in Cybersecurity at ESIEE-IT (France), currently on an exchange semester at the University of Malaya in Kuala Lumpur.

In parallel, I am completing a work-study programme in system integration, which gives me hands-on experience in configuring, deploying, testing and troubleshooting systems.

I am drawn to cybersecurity because I like understanding how systems work, where they fail and how to protect them. In 2023, I simulated a ransomware attack on my own virtual machines to see how such an attack unfolds, and it confirmed my interest. My goal is to become a cybersecurity systems and network engineer with complementary skills in governance, risk and compliance (GRC).

## 2. Technical skills

**Security tools**

| Skill                                            | Level             | Demonstrated in                                  |
| ------------------------------------------------ | ----------------- | ------------------------------------------------ |
| Nmap (host discovery, port and version scanning) | Working knowledge | [Nmap service scan](projects/nmap-service-scan/) |
| Kali Linux                                       | Working knowledge | [Virtual lab setup](projects/virtual-lab-setup/) |
| Burp Suite                                       | Working knowledge | Course practical work                            |
| Metasploit Framework                             | Beginner          | Course practical work                            |
| Wireshark                                        | Beginner          | Course practical work                            |
| Cyberwatch (vulnerability scanning)              | Beginner          | Course practical work                            |

**Systems and networking**

| Skill                                                       | Level             | Demonstrated in                                  |
| ----------------------------------------------------------- | ----------------- | ------------------------------------------------ |
| Virtualisation (VirtualBox, host-only / NAT networking)     | Working knowledge | [Virtual lab setup](projects/virtual-lab-setup/) |
| Networking fundamentals (IP addressing, subnets, isolation) | Working knowledge | [Virtual lab setup](projects/virtual-lab-setup/) |
| Linux command line                                          | Working knowledge | [Virtual lab setup](projects/virtual-lab-setup/) |
| PKI and TLS certificates                                    | Working knowledge | Professional experience                          |

**Programming and scripting**

| Skill  | Level             | Demonstrated in                    |
| ------ | ----------------- | ---------------------------------- |
| Python | Working knowledge | Academic and professional projects |
| Java   | Working knowledge | Academic and professional projects |
| Bash   | Beginner          | Linux administration tasks         |

**Governance and law**

| Skill                                                                   | Level    | Demonstrated in                         |
| ----------------------------------------------------------------------- | -------- | --------------------------------------- |
| ISO 27001, GDPR, risk management                                        | Beginner | Master's coursework                     |
| Malaysian cyber law (Computer Crimes Act 1997, Cyber Security Act 2024) | Beginner | [Learning journey](#5-learning-journey) |

## 3. Certifications and training

No professional cybersecurity certification earned yet.

**Planned**

| Certification / course                       | Status  | Target date   |
| -------------------------------------------- | ------- | ------------- |
| Cisco Networking Academy — Networking Basics | Planned | February 2027 |
| Cisco CCNA (200-301)                         | Planned | June 2027     |

**Education**

| Qualification                                     | Institution                    | Status      |
| ------------------------------------------------- | ------------------------------ | ----------- |
| Master's degree in Cybersecurity (M1)             | ESIEE-IT, France               | In progress |
| International exchange semester                   | University of Malaya, Malaysia | 2026–2027   |
| Bachelor's degree in Web Development and Security | Coding Factory by ESIEE-IT     | Completed   |
| TOEIC English test — 695/990                      | ETS                            | 2026        |

## 4. Projects

| Project                                          | Summary                                                                                                                                                      |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Virtual lab setup](projects/virtual-lab-setup/) | An isolated host-only lab (VirtualBox, Kali Linux, Metasploitable 2), with isolation verified by connectivity tests.                                         |
| [Nmap service scan](projects/nmap-service-scan/) | A full-port service scan of Metasploitable 2: 30 open ports analysed, including the vsftpd 2.3.4 backdoor (CVE-2011-2523), with remediation recommendations. |

## 5. Learning journey

**Ethics and the law.** The first topic that changed my view of the field was the legal framework. In Malaysia, the Computer Crimes Act 1997 makes unauthorised access to a computer an offence, and the Cyber Security Act 2024 requires penetration testing and SOC providers to hold a licence. I took from this that what separates a security professional from an attacker is not the technique, but written authorisation and a clearly defined scope. A single wrong IP address in a scan can be enough to leave that scope.

**Building and scanning my own lab.** In the hands-on lab, I built an isolated environment in VirtualBox with Kali Linux as the attacker and Metasploitable 2 as the target, on a host-only network. A full service scan (`nmap -sV -p-`) found 30 open ports, including Telnet, software almost 20 years old and vsftpd 2.3.4, a version known to contain a backdoor (CVE-2011-2523). The lesson was twofold: a single scan reveals a large attack surface, but a version number alone does not prove a vulnerability. For UnrealIRCd and Samba, Nmap did not give enough detail for me to confirm anything.

**Something that went wrong.** While building the lab, I found that the official Kali image enables a second network adapter in NAT mode by default. The VM therefore had Internet access, and my "isolated" lab was not isolated. When I tried to disable the adapter, the settings were greyed out; the cause was that the VM was in a saved state rather than powered off. After discarding the saved state, I applied the change and verified the result: the ping to Metasploitable succeeded, while pings to 8.8.8.8, my router and my Wi-Fi address failed with "Network is unreachable". I now treat a configuration as correct only once I have tested it.

**What I still find challenging.** Networking beyond the basics (routing, VLANs, ACLs, VPNs and segmentation) is my main gap. The NotPetya case study showed me why it matters: Maersk's flat network allowed the malware to reach its global operations, and about 4,000 servers and 45,000 PCs had to be rebuilt. For the role I am aiming for, this is the skill I most need to strengthen.

**My improvement goal.** By **22 February 2027**, I will review TCP/IP, subnetting, VLANs, routing and ACLs, and publish at least three documented Packet Tracer or GNS3 labs in this portfolio (VLAN segmentation, inter-VLAN routing and ACL filtering). I will measure progress by the labs published here, each with its topology, configuration and verification tests.

## 6. Career objective

**Target role:** Cybersecurity Systems and Network Engineer.

I want to secure IT infrastructures by integrating, hardening and auditing firewalls, VPNs, switches and servers. This role builds directly on my work-study experience in system integration. In the longer term, I want to add security architecture and GRC skills, so that I understand both the technical choices and the security requirements of an organisation.

**Next steps**

1. Strengthen my networking skills and pass the Cisco CCNA (target: June 2027).
2. After my work-study ends in August 2027, apply for a first network security role, while practising firewall configuration, site-to-site VPNs, system hardening and log monitoring with Wazuh or Graylog.
3. From 2028, prepare the CCNP Security and study ISO 27001 and risk analysis.

## 7. Contact

- **GitHub:** [doudouux](https://github.com/doudouux)
- **LinkedIn:** [Dounya Berramdane](https://www.linkedin.com/in/dounya-berramdane-developpeur-informatique/)
- **Email:** dounya.berramdanepro@gmail.com
