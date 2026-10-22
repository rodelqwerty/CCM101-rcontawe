
# System Baseline Report

## Mission Overview

This report records the initial system resources of the Linux server before deploying the client website.

## Memory Check

**Command executed:** `free -h`

- **Total RAM:** 1.9 GiB
- **Used RAM:** 404 MiB
- **Free RAM:** 1.2 GiB
- **Available RAM:** 1.5 GiB

**Screenshot:** `screenshots/memory-check.png`

## Disk Capacity Check

**Command executed:** `df -h /`

- **Total Storage Capacity of Root (`/`) Filesystem:** 19 GiB
- **Used Disk Space:** 5.5 GiB
- **Available Disk Space:** 13 GiB
- **Disk Usage:** 30%

**Screenshot:** `screenshots/disk-check.png`

## CPU and Process Monitoring

**Command executed:** `top`

The `top` command is used to monitor CPU utilization, system load, memory usage, and active processes.

**Screenshot:** `screenshots/cpu-process-monitoring.png`

## Why Is Disk Space Important?

Checking disk space before a massive traffic surge is critical because insufficient storage can prevent the server from writing logs, caching data, and storing necessary files, potentially causing website errors or service interruptions.

## Conclusion

The server has 1.9 GiB of total RAM and 19 GiB of root filesystem storage, with 13 GiB of disk space available. These baseline values provide a reference for monitoring system resources before and during website deployment.
