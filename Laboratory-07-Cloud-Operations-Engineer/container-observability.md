
# Container Observability Report

## Mission Overview

This report documents the Nginx container's application logs and real-time resource metrics. The goal is to verify HTTP request activity and observe the resources consumed by the client website.

## Application Logging

**Command executed:**

```bash
docker logs client-website
```

The container logs were examined to identify successful HTTP requests and the intentionally generated 404 error.

### HTTP 404 Error Log

Copy the actual matching line from your terminal containing `hidden-admin-page` and status `404`:

```text
[Paste the actual log line containing hidden-admin-page and status 404]
```

### Why Are Application Logs Important?

Application logs record events and requests that help engineers understand what happened when an application encounters a problem. They make troubleshooting easier by providing evidence of successful requests, failed requests, and other application activity.

**Screenshot:** `screenshots/docker-logs.png`

## Real-Time Container Metrics

**Command executed:**

```bash
docker stats
```

The `docker stats` command was used to monitor the real-time resource consumption of the running `client-website` container.

### Recorded Container Metrics

| Metric | Actual Value |
|---|---|
| Container Name | `client-website` |
| Container ID | `822c6e8fb463` |
| CPU Usage | 0.00% |
| Memory Usage | 2.727 MiB |
| Memory Limit | 1.859 GiB |
| Memory Usage Percentage | 0.14% |
| Network Input / Received | 3.77 kB |
| Network Output / Transmitted | 5.21 kB |
| Block I/O | 0 B / 12.3 kB |
| Active Processes (PIDs) | 2 |

**Screenshot:** `screenshots/container-metrics.png`

### Resource Usage Analysis

At the time of the screenshot, the `client-website` container was consuming **2.727 MiB of memory** and **0.00% CPU**. Its memory usage was only 0.14% of the displayed 1.859 GiB limit, indicating low resource consumption at the time of measurement.

The container recorded 3.77 kB of received network traffic and 5.21 kB of transmitted network traffic. These values provide a snapshot of the container's network activity and resource utilization.

## Conclusion

Application logs help explain individual events and errors, while container metrics show the resources consumed by the running service. The recorded metrics show that the Nginx `client-website` container was using 2.727 MiB of memory and 0.00% CPU at the time of the screenshot. Together, these observations provide useful evidence for assessing the health and performance of the containerized website.
