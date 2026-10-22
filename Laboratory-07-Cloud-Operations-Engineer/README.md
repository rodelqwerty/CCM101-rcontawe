
# Laboratory 07 — The Cloud Operations Engineer

## Mission Overview

This laboratory activity focuses on monitoring a Linux host and a Dockerized web application. An Nginx container named `client-website` is deployed, HTTP requests are generated, application logs are analyzed, and real-time container resource metrics are collected.

The purpose of this activity is to understand how cloud operations engineers monitor system health, troubleshoot web application errors, and evaluate container resource consumption.

## Objectives

- Monitor Linux memory usage and disk capacity.
- Observe CPU utilization, system load, and running processes.
- Deploy an Nginx web server using Docker.
- Generate successful HTTP requests and an intentional HTTP 404 error.
- Retrieve and analyze application access logs.
- Measure container CPU, memory, and network usage.
- Document system health, monitoring results, and operational findings.
- Organize screenshots and technical documentation for a GitHub portfolio.

## Monitoring Commands Executed

The following commands were used to inspect the Linux host, deploy the Nginx container, simulate HTTP requests, and monitor application performance.

### 1. Linux System Monitoring

Check memory usage:

```bash
free -h
```

Check root filesystem capacity:

```bash
df -h /
```

Monitor CPU utilization and running processes:

```bash
top
```

### 2. Docker Container Deployment

Deploy the Nginx web server:

```bash
docker run -d --name client-website -p 8080:80 nginx
```

Verify that the container is running:

```bash
docker ps
```

### 3. HTTP Request Simulation

Send a request to the Nginx homepage:

```bash
curl -i http://localhost:8080/
```

Generate additional successful HTTP requests:

```bash
curl -i "http://localhost:8080/?visit=2"
curl -i "http://localhost:8080/?visit=3"
```

Generate an intentional HTTP 404 error:

```bash
curl -i http://localhost:8080/hidden-admin-page
```

### 4. Application Log Monitoring

Retrieve the container logs:

```bash
docker logs client-website
```

Examine the logs to identify successful requests and the intentionally generated 404 response.

### 5. Container Resource Monitoring

Display real-time container resource usage:

```bash
docker stats
```

The command displays CPU usage, memory consumption, memory limits, network I/O, block I/O, and the number of active processes.

## System Baseline Results

### Memory Usage

**Command:** `free -h`

| Metric | Recorded Value |
|---|---:|
| Total RAM | 1.9 GiB |
| Used RAM | 404 MiB |
| Free RAM | 1.2 GiB |
| Available RAM | 1.5 GiB |

### Disk Capacity

**Command:** `df -h /`

| Metric | Recorded Value |
|---|---:|
| Root Filesystem | `/dev/vda1` |
| Total Storage | 19 GiB |
| Used Storage | 5.5 GiB |
| Available Storage | 13 GiB |
| Disk Usage | 30% |

These measurements provide a baseline for evaluating the Linux host's resource capacity before and during the deployment.

## Container Observability Results

The `docker stats` command reported the following resource usage for the `client-website` container at the time of the screenshot.

| Metric | Recorded Value |
|---|---:|
| Container Name | `client-website` |
| CPU Usage | 0.00% |
| Memory Usage | 2.727 MiB |
| Memory Limit | 1.859 GiB |
| Memory Usage Percentage | 0.14% |
| Network Input | 3.77 kB |
| Network Output | 5.21 kB |
| Block I/O | 0 B / 12.3 kB |
| Active Processes (PIDs) | 2 |

**Observation:** The Nginx container was consuming 2.727 MiB of memory and 0.00% CPU at the time of measurement, indicating low resource consumption during the observation period.

## Why Is Disk Space Important?

Monitoring disk space before a massive traffic surge is critical because insufficient storage can prevent applications from writing logs, storing files, and creating temporary data, potentially resulting in website errors or service interruptions.

## Skills Learned

- Linux system monitoring using `free`, `df`, and `top`.
- Memory usage and disk capacity analysis.
- Docker container deployment and management.
- Running an Nginx web server inside a container.
- HTTP request simulation using `curl`.
- Understanding HTTP status codes, including 404 errors.
- Application access log retrieval and analysis.
- Real-time container resource monitoring using `docker stats`.
- Technical documentation using Markdown.
- Organizing screenshots and maintaining a GitHub portfolio.

## Conclusion

Laboratory 07 demonstrated the importance of monitoring both the Linux host and a containerized web application. Linux commands provided information about memory and disk capacity, while Docker commands were used to deploy Nginx, generate HTTP requests, inspect application logs, and measure container resource consumption.

The results showed that the host had 1.9 GiB of RAM and 19 GiB of root filesystem storage, with 13 GiB available. The Nginx container consumed 2.727 MiB of memory and 0.00% CPU at the time of the recorded measurement.

Overall, this activity strengthened practical skills in Linux administration, Docker deployment, application troubleshooting, resource monitoring, and technical documentation. These skills are essential for maintaining reliable and efficient cloud-based services.
