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

Copy the actual matching line from your terminal below:

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

Record the values shown for the `client-website` container:

- Container name: `client-website`
- CPU usage: [Enter the actual CPU percentage]
- Memory usage: [Enter the actual memory usage and limit, if displayed]
- Network I/O: [Enter the displayed received and transmitted values]

**Screenshot:** `screenshots/container-metrics.png`

## Conclusion

Application logs help explain individual events and errors, while container metrics show the resources consumed by the running service. Both provide useful evidence when assessing the health of a containerized application.
