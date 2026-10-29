
# Container Observability Report

## 1. Introduction

This report documents application logging and resource monitoring for the `client-website` Nginx container deployed during CCM101 Laboratory Activity 7. The purpose is to examine HTTP requests, identify errors, and monitor the container's resource consumption using Docker.

## 2. Application Logging

### Command Executed

```bash
docker logs client-website
```

The `docker logs` command retrieves the container's logs, allowing the operator to inspect application startup messages, HTTP requests, and errors.

### HTTP Request Results

The Nginx web server processed four HTTP requests during the test:

| Request | HTTP Status | Result |
|---|---|---|
| `GET /` | 200 | Successful |
| `GET /` | 200 | Successful |
| `GET /` | 200 | Successful |
| `GET /hidden-admin-page` | 404 | Not Found |

### HTTP 404 Error Log

The following line was captured from the actual container logs:

```text
172.17.0.1 - - [29/Oct/2026:16:04:02 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

The HTTP 404 error occurred because the requested `/hidden-admin-page` resource did not exist on the Nginx web server.

Application logs are vital for troubleshooting because they record requests and errors that help operators identify what happened during a failure. They provide evidence that can be used to investigate problems, determine possible causes, and verify whether corrective actions resolve an issue.

## 3. Real-Time Container Metrics

### Command Executed

```bash
docker stats
```

The `docker stats` command displays live resource consumption for running containers, including CPU usage, memory usage, network I/O, block I/O, and the number of processes.

### Recorded Container Metrics

The following measurements were captured from the `client-website` container:

| Metric | Recorded Value |
|---|---|
| Container Name | `client-website` |
| CPU Usage | 0.00% |
| Memory Usage | 2.715 MiB |
| Memory Limit | 1.859 GiB |
| Memory Usage Percentage | 0.14% |
| Network I/O | 3.84 kB received / 5.29 kB transmitted |
| Block I/O | 0 B read / 12.3 kB written |
| Processes (PIDs) | 2 |

### Metrics Analysis

At the time of observation, the container was using 0.00% CPU and 2.715 MiB of memory, equivalent to 0.14% of its displayed memory limit. The recorded network I/O was 3.84 kB received and 5.29 kB transmitted.

These results indicate low resource consumption during the test. However, the measurements represent a snapshot of the container's activity and do not establish how it would perform under a large increase in traffic.

## 4. Evidence

The following screenshots document the container's logging and monitoring results:

- `screenshots/docker-logs.png` — Shows the application logs, including the HTTP 404 request.
- `screenshots/container-metrics.png` — Shows the Docker resource usage metrics.

## 5. Analysis

Application logs and resource metrics provide different but complementary information. Logs show individual requests, events, and errors, while metrics quantify resource consumption and performance.

In this activity, the logs confirmed that the Nginx container successfully processed three requests with HTTP 200 status codes and returned HTTP 404 for the nonexistent page. The Docker metrics showed low CPU and memory consumption during the observation period.

Combining logs and metrics helps cloud operations engineers investigate application errors, monitor system health, and identify potential performance issues.

## 6. Conclusion

This activity provided practical experience in application logging and container monitoring. The `docker logs` command helped identify the HTTP 404 response, while `docker stats` provided information about CPU, memory, network, and block I/O usage.

These observability techniques are important for maintaining reliable containerized applications and troubleshooting problems in cloud environments.

