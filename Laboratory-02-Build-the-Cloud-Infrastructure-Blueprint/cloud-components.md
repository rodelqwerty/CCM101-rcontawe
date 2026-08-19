# Checkpoint 3 – Identify Cloud Infrastructure Components

Based on the data I gathered from KillerCoda, I discovered four primary elements of cloud infrastructure: **Processing, Data Storage, Connectivity, and System Software**.

---

## 1. Compute Resources

**Example:** CPU and RAM

| **Compute Information** | **Details**       |
| ----------------------- | ----------------- |
| **CPU**                 | Intel Xeon E312xx |
| **CPU(s)**              | 1                 |
| **RAM**                 | 1.9 GiB           |


**Purpose:**

CPU and RAM are used to run programs and perform tasks on the server.

**Why it is important in cloud computing:**

Cloud servers need memory and processors to run programs. When an application needs more power, more processors and memory can be added.

**In KillerCoda:**

The KillerCoda server is equipped with 1 processor and 1.9 GiB of memory. These specifications enable the Ubuntu operating system and its operations to function smoothly.
**---

## 2. Storage Resources

**Example:** Virtual Disk

**From KillerCoda:**

| **Storage Information** | **Details** |
| ----------------------- | ----------- |
| **Disk**                | `/dev/vda1` |
| **Size**                | 19 GB       |
| **Available**           | 13 GB       |
| **File System**         | ext4        |


**Purpose:**

The function of storage is to retain files, applications, and the system software

**Why it is important in cloud computing:**

Maintaining important documents and application data depends on storage on cloud servers.

**In KillerCoda:**

In The server has a 19 GB virtual hard drive. The main storage is on ext4 filesystem and is found at `/`.
**---

## 3. Networking Resources

**Example:** Network Interface and IP Address

**From KillerCoda:**

| **Network Information** | **Details**  |
| ----------------------- | ------------ |
| **Network Interface**   | `enp1s0`     |
| **IP Address**          | `172.30.1.2` |
| **Docker Network**      | `docker0`    |
| **Docker IP**           | `172.17.0.1` |


**Purpose:**

The server may connect with other systems and services via networking.

**Why it is important in cloud computing:**

Network access is needed for users and many services to interact with cloud servers.

**In KillerCoda:**

**The main network interface is enp1s0; its IP address is 172.30.1.2. The server also has a `docker0` network that lets Docker do its thing.
**---

## 4. Operating System

**Example:** Ubuntu Linux

**From KillerCoda:**

| **Operating System Information** | **Details**        |
| -------------------------------- | ------------------ |
| **Operating System**             | Ubuntu 24.04.4 LTS |
| **Kernel Version**               | 6.8.0-136-generic  |


**Purpose:**
The operating system controls the computer's hardware and makes application running possible.

**Why it is important in cloud computing:**

To guarantee that apps run properly, the system software controls the central processing unit, random access memory, data storage, and connectivity.

**In KillerCoda:**

**Ubuntu 24.04.4 LTS powers the server. Ubuntu handles the networking features, memory, storage capacity, and main processor of the server.
**---

| **Component**        | **KillerCoda Example** | **What It Does**                        |
| -------------------- | ---------------------- | --------------------------------------- |
| **Compute**          | 1 CPU, 1.9 GiB RAM     | Runs tasks and programs                 |
| **Storage**          | 19 GB disk             | Stores files and data                   |
| **Networking**       | `enp1s0`, `172.30.1.2` | Lets the server connect and communicate |
| **Operating System** | Ubuntu 24.04.4 LTS     | Manages the whole server                |

**In Simple Terms**

The CPU and RAM help the server run programs, storage keeps files and data, networking lets the server communicate, and the operating system manages everything.
