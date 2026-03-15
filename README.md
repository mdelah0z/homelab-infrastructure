# Homelab Infrastructure

This repository documents my personal IT infrastructure lab used for learning and testing enterprise systems administration, virtualization, and network services.

The environment simulates a small enterprise infrastructure including virtualization hosts, Linux servers, and Windows Server services.

---

# Infrastructure Overview

**Network:** 192.168.18.0/24

| Host              | IP Address     | Role                                  |
| ----------------- | -------------- | ------------------------------------- |
| Local Host        | 192.168.18.46  | Main workstation                      |
| Ubuntu VM         | 192.168.18.80  | Connectivity testing                  |
| ESXi1             | 192.168.18.90  | Primary virtualization host           |
| ESXi2             | 192.168.18.91  | Testing environment for risky changes |
| vCenter           | 192.168.18.100 | VMware virtualization management      |
| DNS Server        | 192.168.18.110 | Internal DNS server (CentOS Stream)   |
| WinSer-DC1        | 192.168.18.30  | Active Directory Domain Controller    |
| WinSer-DC2        | 192.168.18.35  | Active Directory Domain Controller    |
| CentOS Stream Lab | 192.168.18.59  | Linux testing server                  |
| Linux Mint JP     | 192.168.18.64  | Office server connected to 1TB USB NAS    |

---

# Virtualization Platform

The homelab uses multiple virtualization platforms to simulate a small enterprise infrastructure environment.

### Host Hypervisors

The following platforms are used to run virtual machines directly on the workstation:

* VMware Workstation Pro
* Oracle VirtualBox

---

# Core Services

The homelab currently provides the following infrastructure services:

* Active Directory Domain Services
* Internal DNS server
* VMware virtualization environment
* Linux administration lab
* Network connectivity testing environment

---

# Lab Objectives

This homelab is used to practice and improve skills related to:

* Enterprise infrastructure deployment
* Virtualization administration
* Linux server configuration and administration
* Windows Server configuration and administration
* Active Directory infrastructure
* DNS server configuration
* Troubleshooting and operational support

---

# Technology Stack

### Virtualization

* VMware Workstation Pro
* Oracle VirtualBox
* VMware ESXi
* VMware vCenter

### Operating Systems

* Windows Server
* CentOS Stream
* Ubuntu
* Linux Mint

### Infrastructure Services

* Active Directory Domain Services
* DNS

# Planned Improvements

Future projects planned for this environment include:

* Infrastructure monitoring deployment
* Automated backups
* Infrastructure documentation improvements
* Additional Linux services


