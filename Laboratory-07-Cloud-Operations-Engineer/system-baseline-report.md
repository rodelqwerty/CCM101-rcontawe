
# System Baseline Report

## Mission Overview

This report documents the initial health and resource capacity of the Linux server before deploying the client's website using Nginx. The baseline assessment includes memory usage, root filesystem capacity, and CPU and process monitoring. These measurements provide a reference for evaluating the server's performance during the laboratory activity.

## Memory Check

**Command executed:** `free -h`

The `free -h` command was used to check the server's memory capacity and current memory usage.

| Memory Information | Result |
|---|---:|
| Total RAM | 1.9 GiB |
| Used RAM | 404 MiB |
| Free RAM | 1.2 GiB |
| Shared Memory | 1.1 MiB |
| Buffer/Cache | 457 MiB |
| Available RAM | 1.5 GiB |
| Total Swap | 1.0 GiB |
| Used Swap | 0 B |
| Free Swap | 1.0 GiB |

**Screenshot:** `screenshots/memory-check.png`

**Observation:**

The server has 1.9 GiB of total RAM, with 404 MiB currently in use and approximately 1.5 GiB available. This indicates that the server has sufficient available memory for the initial stage of the laboratory activity. The swap space is also available, with no swap memory currently being used.

## Disk Capacity Check

**Command executed:** `df -h /`

The `df -h /` command was used to check the capacity and usage of the root filesystem.

| Disk Information | Result |
|---|---:|
| Filesystem | `/dev/vda1` |
| Total Capacity | 19 GiB |
| Used Disk Space | 5.5 GiB |
| Available Disk Space | 13 GiB |
| Disk Usage | 30% |
| Mount Point | `/` |

**Screenshot:** `screenshots/disk-check.png`

**Observation:**

The root filesystem has a total capacity of 19 GiB, with 5.5 GiB used and approximately 13 GiB available. Disk usage is currently at 30%, indicating that sufficient storage remains for the Nginx web server, website files, logs, and other required resources.

## CPU and Process Monitoring

**Command executed:** `top`

The `top` command was used to monitor CPU utilization, system load, memory usage, and active processes in real time.

**Observation:**

The `top` command provides a live overview of the server's performance. It helps identify resource-intensive processes and determine whether the CPU or memory is under heavy load. This information is useful for monitoring the server before and during website deployment.

**Screenshot:** `screenshots/cpu-process-monitoring.png`

## Why Is Disk Space Important?

Checking disk space before a traffic surge is important because a server needs sufficient storage to operate reliably. If the disk becomes full, applications may fail to write logs, store uploaded files, create temporary files, or perform other essential operations.

For a website hosted using Nginx, monitoring disk capacity helps prevent storage-related service interruptions and ensures that sufficient space remains available for website files, logs, and future updates. Regular monitoring also helps administrators identify when additional storage or cleanup may be necessary.

## Conclusion

The baseline assessment shows that the Linux server has 1.9 GiB of RAM, approximately 1.5 GiB of available memory, and 13 GiB of available root filesystem storage. Disk usage is at 30%, and no swap memory is currently being used.

Based on these initial measurements, the server has available memory and disk capacity for the initial Nginx deployment. However, actual performance will depend on the website's workload, traffic volume, and the resources consumed by running services.

These baseline measurements will serve as a reference for comparing system resource usage during the laboratory activity and identifying potential performance or capacity issues.
