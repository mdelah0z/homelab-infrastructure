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

# Configuration Files

Main configuration file:

```
/etc/named.conf
```

Zone files directory:

```
/var/named/
```

Zone configuration:

```
zone "lab.local" IN {
    type master;
    file "lab.local.db";
    allow-update { none; };
};
```

---

# Example DNS Records

Entries in the internal zone file:

```
[root@localhost named]# cat lab.local.db
$TTL 86400
@   IN  SOA     ns1.lab.local. admin.lab.local. (
        2026030504
        3600
        1800
        604800
        86400 )

@       IN  NS      ns1.lab.local.

ns1     IN  A       192.168.18.110
dns     IN  A       192.168.18.110
esxhost1  IN  A       192.168.18.90
esxhost2     IN  A       192.168.18.91
esxvcenter      IN A    192.168.18.100
centos9stl      IN A    192.168.18.59
centos9dns      IN A    192.168.18.110
winser-dc1      IN A    192.168.18.30
winser-dc2      IN A    192.168.18.35
linuxmintjp     IN A    192.168.18.64
[root@localhost named]#
```
