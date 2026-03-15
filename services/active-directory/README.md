
# Active Directory Infrastructure

This document describes the Active Directory deployment used in the homelab environment.

---

# Domain Information

| Parameter               | Value               |
| ----------------------- | ------------------- |
| Domain Name             | ad.lab.local           |
| Forest Functional Level | Windows Server 2025 |
| Domain Functional Level | Windows Server 2025 |

The domain provides centralized authentication and directory services for the homelab infrastructure.

---

# Domain Controllers

| Server     | IP Address    | Role                        |
| ---------- | ------------- | --------------------------- |
| WinSer-DC1 | 192.168.18.30 | Primary Domain Controller   |
| WinSer-DC2 | 192.168.18.35 | Secondary Domain Controller |

Both systems run Windows Server and host the Active Directory Domain Services role.

---

# Active Directory Services

The following services are provided by the domain controllers:

* Active Directory Domain Services
* DNS integration
* Domain authentication
* Directory services

---

# Infrastructure Integration

Active Directory interacts with the following systems in the homelab:

| System                | Purpose                            |
| --------------------- | ---------------------------------- |
| DNS Server            | Internal name resolution           |
| Windows Workstations | User authentication |

---

# Replication

Active Directory replication ensures that directory data is synchronized between domain controllers.

Replication occurs automatically between:

* WinSer-DC1
* WinSer-DC2

This setup allows testing redundancy and domain controller failover scenarios.

---

# Administrative Tools

Common tools used to manage the Active Directory environment:

* Active Directory Users and Computers
* Active Directory Sites and Services
* Active Directory Domains and Trusts
* Group Policy Management

---

# Validation

The following checks were performed to validate the domain infrastructure:

* Domain controllers successfully joined to the domain
* DNS records automatically registered
* Replication between domain controllers functioning correctly
* Domain authentication tested with domain users

---

# Future Improvements

Planned improvements for the Active Directory infrastructure include:

* Additional organizational units
* Group policy configuration

