
# Mission Reflection

## Cloud Operations Engineer Reflection

This laboratory activity helped me understand why monitoring is an important part of cloud computing. I learned that deploying an application is not enough because the server and the application must also be monitored to ensure that they continue working properly.

Checking the host server's resources is important even when containers are running perfectly. Containers depend on the host's CPU, memory, and storage. If the host runs out of memory or disk space, the application may become slow, fail to save logs, or stop working. Checking these resources before a large increase in traffic helps identify possible limitations early.

The `docker logs` command is useful when a user reports that they cannot log in to a web application. It allows an operator to inspect the available application logs and look for errors, failed requests, or other events related to the problem. Although the logs do not always reveal the complete cause, they provide useful evidence for further investigation.

I also learned the difference between logs and metrics. Logs describe individual events, requests, and errors, while metrics show numerical measurements such as CPU usage, memory consumption, and network activity. Logs help explain what happened, while metrics help show how the system is performing.

Large enterprise companies can use monitoring platforms such as Prometheus and Grafana to monitor thousands of containers. Prometheus can collect and store metrics, while Grafana can display them in dashboards. Alerts can also notify operations teams when resource usage or other measurements exceed defined thresholds.

My ability to troubleshoot Linux environments improved through using commands such as `free -h`, `df -h /`, `top`, `docker logs`, and `docker stats`. I gained practical experience checking system resources, deploying Nginx, generating HTTP requests, and identifying a 404 error. Overall, this activity helped me understand how monitoring and observability support reliable cloud services.

