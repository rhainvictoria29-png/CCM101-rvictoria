
# Laboratory 07: Cloud Operations Engineer

**Course:** CCM101 – Cloud Computing  
**Mission:** Mission 7 – The Cloud Operations Engineer  
**Environment:** KillerCoda Ubuntu Playground and Docker

## 1. Mission Overview

This laboratory activity focuses on cloud operations, system monitoring, and application observability. Acting as a Cloud Operations Engineer at the fictional CloudNova Technologies, I established a baseline for the Linux host, deployed an Nginx web server container, generated HTTP requests, examined application logs, and monitored container resource consumption.

The purpose of this activity was to understand how system information, logs, and metrics help operators evaluate application health and troubleshoot problems.

## 2. Objectives

The objectives of this laboratory activity were to:

- Monitor host memory, disk capacity, CPU activity, and running processes.
- Deploy an Nginx web server using Docker.
- Generate successful HTTP requests and an intentional HTTP 404 error.
- Retrieve and analyze container application logs.
- Monitor CPU, memory, and network usage using Docker metrics.
- Document technical findings and evidence in Markdown.
- Maintain a structured GitHub Cloud Computing Portfolio.

## 3. Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Check host memory usage. |
| `df -h /` | Check root filesystem capacity. |
| `top` | Observe CPU activity and running processes. |
| `docker run -d --name client-website -p 8080:80 nginx` | Deploy the Nginx container. |
| `docker ps` | Verify running containers and port mappings. |
| `curl -i http://localhost:8080/` | Test the web server using HTTP requests. |
| `curl -i http://localhost:8080/hidden-admin-page` | Generate an HTTP 404 response. |
| `docker logs client-website` | Retrieve application logs. |
| `docker stats` | Monitor live container resource usage. |

## 4. Skills Learned

Through this activity, I practiced Linux system monitoring, Docker container deployment, HTTP testing, application log analysis, and real-time resource monitoring. I also improved my ability to document technical results and organize evidence using GitHub and Markdown.

The activity demonstrated how logs and metrics provide different but complementary information for evaluating the health of a containerized application.

## 5. Repository Contents

- `system-baseline-report.md` — Host resource measurements.
- `container-observability.md` — Application logs and container metrics.
- `reflection.md` — Personal learning reflection.
- `screenshots/` — Evidence collected during the laboratory activity.

## 6. Conclusion

This laboratory activity provided practical experience with essential cloud operations tasks. Monitoring the host and the application container helped demonstrate why resource measurements, logs, and structured technical documentation are important for maintaining reliable services.

