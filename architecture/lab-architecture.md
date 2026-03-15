# Lab Architecture

This document describes the architecture of the homelab infrastructure.

---

# Network

Network range:

192.168.18.0/24

This network contains the workstation, hypervisors, infrastructure services, and Linux test machines.

---

# Workstation Layer

| System     | IP            | Role                                                 |
| ---------- | ------------- | ---------------------------------------------------- |
| Local Host | 192.168.18.46 | Primary workstation hosting virtualization platforms |

Virtualization platforms running on the workstation:

* VMware Workstation Pro
* Oracle VirtualBox

---

# Virtualization Infrastructure

Nested virtualization is used to simulate a VMware enterprise infrastructure.

| System  | IP             | Role                                             |
| ------- | -------------- | ------------------------------------------------ |
| ESXi1   | 192.168.18.90  | Primary hypervisor hosting infrastructure VMs    |
| ESXi2   | 192.168.18.91  | Secondary hypervisor used for testing changes    |
| vCenter | 192.168.18.100 | Centralized management for VMware infrastructure |

This setup allows testing multi-host VMware environments.

---

# Infrastructure Services

| Service                  | Host          | IP             |
| ------------------------ | ------------- | -------------- |
| Active Directory         | WinSer-DC1    | 192.168.18.30  |
| Active Directory Replica | WinSer-DC2    | 192.168.18.35  |
| DNS Server               | CentOS Stream | 192.168.18.110 |

These systems simulate enterprise directory and name resolution services.

---

# Linux Lab Systems

| System            | IP            | Purpose                        |
| ----------------- | ------------- | ------------------------------ |
| Ubuntu VM         | 192.168.18.80 | Connectivity testing           |
| CentOS Stream Lab | 192.168.18.59 | Linux administration practice  |
| Linux Mint JP     | 192.168.18.64 | Office services and NAS access |

---

