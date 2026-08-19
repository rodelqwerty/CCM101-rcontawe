# Infrastructure Report

## Checkpoint 2 – Investigate the Cloud Server

I used the KillerCoda terminal to check the server's operating system, hardware, network, and storage information.

---

## 1. Server Information

### Operating System

**Command used:**

```bash
cat /etc/os-release
```

**Result:**

* OS: Ubuntu 24.04.4 LTS
* Version: 24.04
* Codename: Noble Numbat

---

### Kernel Version

**Command used:**

```bash
uname -r
```

**Result:**

* Kernel: 6.8.0-136-generic

---

### CPU Model

**Command used:**

```bash
lscpu | grep "Model name"
```

**Result:**

* CPU: Intel Xeon E312xx (Sandy Bridge, IBRS update)

---

### Number of CPU Cores

**Command used:**

```bash
lscpu | grep "^CPU(s):"
```

**Result:**

* CPU(s): 1

---

### Total RAM

**Command used:**

```bash
free -h
```

**Result:**

* Total RAM: 1.9 GiB
* Used: 421 MiB
* Free: 864 MiB
* Available: 1.4 GiB
* Swap: 1.0 GiB

---

### Hostname

**Command used:**

```bash
hostname
```

**Result:**

* Hostname: ubuntu

---

## 2. Network Information

### IP Address

**Command used:**

```bash
hostname -I
```

**Result:**

* 172.30.1.2
* 172.17.0.1

The main IP address of the server is **172.30.1.2**. The **172.17.0.1** address is for the Docker network.

---

### Network Interfaces

**Command used:**

```bash
ip addr
```

**Result:**

**enp1s0**

* IP Address: 172.30.1.2/24
* Status: UP
* MAC Address: 82:fa:1a:0c:f6:e1

**docker0**

* IP Address: 172.17.0.1/16
* Status: DOWN

**lo**

* IP Address: 127.0.0.1/8
* This is the loopback interface.

---

## 3. Storage Information

### Disk Capacity

**Command used:**

```bash
df -h
```

**Result:**

| Filesystem | Size | Used | Available | Use% | Mounted on |
| ---------- | ---: | ---: | --------: | ---: | ---------- |
| /dev/vda1  |  19G | 5.4G |       13G |  30% | /          |
| /dev/vda16 | 881M | 117M |      703M |  15% | /boot      |
| /dev/vda15 | 105M | 6.2M |       99M |   6% | /boot/efi  |

The main disk is **19 GB** and is mounted on `/`.

---

### Mounted File Systems

**Command used:**

```bash
findmnt
```

**Main mounted file systems:**

| Mount Point | Source     | File System |
| ----------- | ---------- | ----------- |
| `/`         | /dev/vda1  | ext4        |
| `/boot`     | /dev/vda16 | ext4        |
| `/boot/efi` | /dev/vda15 | vfat        |
| `/proc`     | proc       | proc        |
| `/sys`      | sysfs      | sysfs       |
| `/dev`      | udev       | devtmpfs    |
| `/run`      | tmpfs      | tmpfs       |
| `/dev/shm`  | tmpfs      | tmpfs       |

---

## Summary

| Information       | Finding                                       |
| ----------------- | --------------------------------------------- |
| Operating System  | Ubuntu 24.04.4 LTS                            |
| Kernel Version    | 6.8.0-136-generic                             |
| CPU Model         | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| CPU(s)            | 1                                             |
| Total RAM         | 1.9 GiB                                       |
| Disk Capacity     | 19 GB                                         |
| Main File System  | ext4                                          |
| Hostname          | ubuntu                                        |
| IP Address        | 172.30.1.2                                    |
| Network Interface | enp1s0                                        |

