
# System Baseline Report

## 1. Introduction

This report documents the initial health check of the Linux host environment used for CCM101 Laboratory Activity 7. The purpose is to identify available system resources before deploying a containerized web server.

## 2. Memory Usage

Command executed:

```bash
free -h
```

- **Total RAM:** 1.9 Gi
- **Used RAM:** 404 Mi
- **Available RAM:** 1.5 Gi

The `free -h` command displays the host's memory usage in a human-readable format. Based on the output, the server has approximately 1.5 Gi of available memory.

## 3. Disk Storage

Command executed:

```bash
df -h /
```

- **Root filesystem:** /
- **Total storage capacity:** 19G
- **Used storage:** 5.5G
- **Available storage:** 13G
- **Disk usage:** 30%

Checking disk space before a massive traffic surge is important because insufficient storage can prevent applications from writing logs, temporary files, and other required data, potentially causing service failures.

## 4. CPU and Process Monitoring

Command executed:

```bash
top
```

The `top` command is used to observe active processes, CPU utilization, and system load. These measurements help establish an initial understanding of the host's performance.

## 5. Evidence

- `screenshots/memory-check.png`
- `screenshots/disk-check.png`

## 6. Conclusion

The host system baseline shows that the Linux environment has 1.9 Gi of total RAM, approximately 1.5 Gi of available memory, and a root filesystem with 19G of total storage capacity. These measurements provide an initial reference for evaluating the host's resources before running the Nginx container.

