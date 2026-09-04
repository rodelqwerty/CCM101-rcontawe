
# Checkpoint 7 – Linux Investigation and Cloud Migration

## 1. Linux Server Specifications

The following specifications were collected from the KillerCoda Ubuntu Playground.

| Specification        | Details                           |
| -------------------- | --------------------------------- |
| **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat) |
| **Distribution**     | Ubuntu                            |
| **Version**          | 24.04                             |
| **Architecture**     | x86_64                            |
| **CPU**              | 1 CPU                             |
| **CPU Model**        | Intel Xeon E312xx (Sandy Bridge)  |
| **CPU Speed**        | 2.0 GHz                           |
| **CPU Core**         | 1 Core                            |
| **CPU Thread**       | 1 Thread                          |
| **Hypervisor**       | KVM                               |
| **Virtualization**   | Full Virtualization               |
| **RAM**              | 1.9 GiB                           |
| **RAM Used**         | 422 MiB                           |
| **RAM Available**    | 1.4 GiB                           |
| **Swap**             | 1.0 GiB                           |
| **Disk Size**        | 19 GB                             |
| **Disk Used**        | 5.4 GB                            |
| **Disk Available**   | 13 GB                             |
| **Disk Usage**       | 30%                               |

---

# 2. Cloud Services That Could Host the Server

The KillerCoda server is a **virtualized Ubuntu 24.04.4 LTS server** with 1 CPU, 1.9 GiB RAM, and 19 GB of disk space. Since AWS, Azure, and GCP all provide Linux virtual machines, the server can be migrated to any of these platforms.

## ☁️ AWS – Amazon EC2

| Item              | Details                                                                                                                                                                                                                                                                 |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cloud Service** | **Amazon EC2 (Elastic Compute Cloud)**                                                                                                                                                                                                                                  |
| **Can Host It?**  | ✅ Yes                                                                                                                                                                                                                                                                   |
| **Why?**          | Amazon EC2 provides virtual servers that can run Linux operating systems such as Ubuntu. The server's 1 CPU and 1.9 GiB RAM requirements can be matched with a small EC2 instance. Storage can also be configured to provide at least the required 19 GB of disk space. |
| **Suitable For**  | Ubuntu servers, websites, applications, and development environments.                                                                                                                                                                                                   |
| **Conclusion**    | **Amazon EC2 can host the KillerCoda Ubuntu server.**                                                                                                                                                                                                                   |

---

## ☁️ Microsoft Azure – Azure Virtual Machines

| Item              | Details                                                                                                                                                                                                                                           |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cloud Service** | **Azure Virtual Machines**                                                                                                                                                                                                                        |
| **Can Host It?**  | ✅ Yes                                                                                                                                                                                                                                             |
| **Why?**          | Azure Virtual Machines supports Linux operating systems, including Ubuntu. A small Azure VM can be selected to provide CPU and memory similar to the KillerCoda server. Azure managed disks can also provide the required storage for the server. |
| **Suitable For**  | Ubuntu servers, web applications, and Linux-based services.                                                                                                                                                                                       |
| **Conclusion**    | **Azure Virtual Machines can host the KillerCoda Ubuntu server.**                                                                                                                                                                                 |

---

## ☁️ GCP – Compute Engine

| Item              | Details                                                                                                                                                                                                                                                                     |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cloud Service** | **Google Compute Engine**                                                                                                                                                                                                                                                   |
| **Can Host It?**  | ✅ Yes                                                                                                                                                                                                                                                                       |
| **Why?**          | Google Compute Engine provides virtual machines that support Linux operating systems such as Ubuntu. The VM can be configured with enough CPU, memory, and storage to meet the KillerCoda server's requirements. Ubuntu 24.04 LTS can also be used as the operating system. |
| **Suitable For**  | Ubuntu servers, websites, applications, and development environments.                                                                                                                                                                                                       |
| **Conclusion**    | **Google Compute Engine can host the KillerCoda Ubuntu server.**                                                                                                                                                                                                            |

---

# 3. Final Comparison

| Cloud Provider | Cloud Service          | Ubuntu Support | Can Match Server Requirements? |
| -------------- | ---------------------- | -------------- | ------------------------------ |
| **AWS**        | Amazon EC2             | ✅ Yes          | ✅ Yes                          |
| **Azure**      | Azure Virtual Machines | ✅ Yes          | ✅ Yes                          |
| **GCP**        | Compute Engine         | ✅ Yes          | ✅ Yes                          |

