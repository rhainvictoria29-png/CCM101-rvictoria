# Laboratory 03 – Multi-Cloud Explorer

## CCM101 – Cloud Computing

**Mission:** Mission 3 – Become a Multi-Cloud Explorer

---

# 1. Mission Overview

Laboratory Activity 3 focuses on exploring and comparing three major public cloud platforms: Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP).

The purpose of this activity is to understand the core services provided by each cloud provider, compare their capabilities, analyze different business requirements, and recommend appropriate cloud platforms for different organizations.

---

# 2. Mission Objectives

The objectives of this laboratory activity are:

* Explore major public cloud platforms.
* Identify core services offered by AWS, Azure, and GCP.
* Compare cloud services across different providers.
* Analyze business requirements and recommend cloud solutions.
* Create technical documentation using Markdown.
* Continue developing a professional Cloud Computing Portfolio on GitHub.

---

# 3. Cloud Platforms Explored

The three cloud platforms investigated in this laboratory are:

1. Amazon Web Services (AWS)
2. Microsoft Azure
3. Google Cloud Platform (GCP)

Detailed research for each platform can be found in:

* [AWS Research](aws-research.md)
* [Azure Research](azure-research.md)
* [GCP Research](gcp-research.md)

---

# 4. Linux Environment Investigation

A KillerCoda Linux playground was used to investigate the basic system information of a Linux server.

## 4.1 Operating System

Command used:

```bash
cat /etc/os-release
```

### Result

```text
PRETTY_NAME="Ubuntu 24.04.4 LTS"
```

---

## 4.2 CPU Information

Command used:

```bash
lscpu
```

### Important Information

| Information  | Result |
| ------------ | ------ |
| Architecture | x86_64 |
| CPU(s)       | 1      |

---

## 4.3 Memory

Command used:

```bash
free -h
```

### Important Information

| Information      | Result  |
| ---------------- | ------- |
| Total Memory     | 1.9 GiB |
| Used Memory      | 428 MiB |
| Available Memory | 1.4 GiB |
| Swap             | 1.0 GiB |

---

## 4.4 Disk Space

Command used:

```bash
df -h
```

### Important Information

| Information     | Result    |
| --------------- | --------- |
| Main Filesystem | /dev/vda1 |
| Total Size      | 19 GB     |
| Used            | 5.4 GB    |
| Available       | 13 GB     |
| Usage           | 30%       |
| Mounted On      | /         |

The main filesystem `/dev/vda1` contains the primary Linux filesystem and is therefore the most important disk information for this investigation.

---

# 5. Cloud Hosting Options for the Linux Server

If this Linux server were migrated to the cloud, equivalent virtual machine services could be used on all three major cloud platforms.

| Cloud Provider | Possible Service       | Purpose                        |
| -------------- | ---------------------- | ------------------------------ |
| AWS            | Amazon EC2             | Host the Linux virtual machine |
| Azure          | Azure Virtual Machines | Host the Linux virtual machine |
| GCP            | Compute Engine         | Host the Linux virtual machine |

These services provide virtual computing environments where a Linux operating system can be installed and used to run applications and services.

---

# 6. KillerCoda Evidence

The following screenshot shows the Linux investigation performed using KillerCoda.

![KillerCoda Terminal](https://github.com/rhainvictoria29-png/CCM101-rvictoria/blob/main/Laboratory-03-Multi-Cloud-Explorer/Laboratory-03-Multi-Cloud-Explorer/screenshots/Checkpoint%207%20-killercoda-terminal-1.png)
![KillerCoda Terminal](
https://github.com/rhainvictoria29-png/CCM101-rvictoria/blob/main/Laboratory-03-Multi-Cloud-Explorer/Laboratory-03-Multi-Cloud-Explorer/screenshots/Checkpoint%207%20-%20killercoda-terminal-2.png
)

---

# 7. Repository Evidence

The GitHub repository contains the Markdown documentation, research files, comparison tables, recommendations, reflection, and screenshots for this laboratory activity.

![GitHub Repository]([screenshots/github-repository.png](https://github.com/rhainvictoria29-png/CCM101-rvictoria/blob/main/Laboratory-03-Multi-Cloud-Explorer/Laboratory-03-Multi-Cloud-Explorer/screenshots/Checkpoint%201.png
))

---

# 8. Laboratory Files

This laboratory contains the following files:

| File                           | Description                                |
| ------------------------------ | ------------------------------------------ |
| `README.md`                    | Main laboratory documentation              |
| `aws-research.md`              | AWS research                               |
| `azure-research.md`            | Azure research                             |
| `gcp-research.md`              | GCP research                               |
| `cloud-platform-comparison.md` | Cloud provider comparison                  |
| `client-recommendations.md`    | Client recommendations and decision matrix |
| `reflection.md`                | Mission reflection                         |

---

# 9. Conclusion

This laboratory provided an opportunity to explore three major cloud providers and understand how their services can be used to solve different business requirements.

The activity also connected Linux server administration with cloud computing by identifying how a Linux environment could be hosted using virtual machine services from AWS, Azure, and GCP.

Through this activity, I learned how to investigate a Linux environment, compare cloud platforms, and relate Linux virtual machines to cloud computing services.
