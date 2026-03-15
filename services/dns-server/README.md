# Linux DNS Server (BIND)

This document describes the deployment and configuration of the internal DNS server used in the homelab environment.

---

# Server Information

| Parameter        | Value           |
| ---------------- | --------------- |
| Hostname         | dns-server      |
| IP Address       | 192.168.18.110  |
| Operating System | CentOS Stream 9 |
| DNS Software     | BIND            |

The DNS server provides internal name resolution for the homelab infrastructure network.

Network:

192.168.18.0/24

---

# Purpose

This DNS server is used to:

* Resolve internal hostnames
* Simulate enterprise DNS infrastructure
* Provide a testing environment for DNS configuration and troubleshooting

---

# Installation

BIND was installed using the system package manager.

```
sudo dnf install bind bind-utils
```

Enable and start the service:

```
sudo systemctl enable named
sudo systemctl start named
```

Verify the service status:

```
sudo systemctl status named
```

---

