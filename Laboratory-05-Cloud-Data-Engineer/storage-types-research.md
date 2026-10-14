# Checkpoint 2 - Research: Types of Cloud Storage

## Overview

A quick reference guide comparing the three primary cloud storage models, highlighting how they store data, their ideal use cases, and leading provider options.

## Comparison of Cloud Storage Types

| Storage Type | Description | Best Used For | Cloud Provider Examples |
| :--- | :--- | :--- | :--- |
| **Block Storage** | Splitting data into raw, fixed-size chunks (blocks) with unique addresses. Operates like attaching a dedicated virtual hard drive directly to a server. | High-performance, low-latency applications that need fast read/write speeds, such as database storage and virtual machine boot disks. | **Amazon EBS:** Resizable persistent drives for EC2.<br><br>**Azure Managed Disks:** Managed disk volumes for Azure VMs.<br><br>**Google Persistent Disk:** Durable block storage for Compute Engine. |
| **File Storage** | Organizing data using a traditional hierarchical structure of files and folders using a shared path. Operates like an office network drive accessible by multiple devices simultaneously. | Collaborative workflows requiring shared access across multiple instances or users, such as shared code repositories, configuration files, or team media assets. | **Amazon EFS:** Scalable file systems for EC2.<br><br>**Azure Files:** Cloud-based file shares using SMB/NFS.<br><br>**Google Filestore:** High-performance shared file storage for GCP. |
| **Object Storage** | Storing data as self-contained units (objects) containing raw data, a unique identifier, and custom metadata, managed via HTTP APIs without standard folders. Operates like a digital warehouse where files are retrieved via unique pickup keys. | Storing massive volumes of unstructured data (e.g., user uploads, backups, log files, media) cost-effectively with flexible global access. | **Amazon S3:** Scalable, highly durable storage with direct URL access.<br><br>**Azure Blob Storage:** Tiered storage for unstructured data and media.<br><br>**Google Cloud Storage:** Global storage integrated with CDNs and analytics tools. |

---

## Why Object Storage Suits User-Uploaded Images

Object storage solutions like Amazon S3, Azure Blob Storage, or Google Cloud Storage serve as the optimal architecture for handling user-uploaded image files because they are designed specifically for unstructured, write-once media data. This model provides virtually unlimited capacity at a significantly lower cost per gigabyte than block or file storage. Furthermore, images can be served directly to global end-users through HTTP URLs or integrated Content Delivery Networks (CDNs) to bypass application servers, allowing you to store only lightweight URL references in your primary database to maintain optimal performance.
