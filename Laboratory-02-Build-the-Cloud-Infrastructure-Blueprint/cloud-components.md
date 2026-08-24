# Cloud Infrastructure Components

## 1. Compute Resources

### Purpose

Compute resources provide the processing power required to execute applications, commands, and services.

### Importance in Cloud Computing

Compute resources are important because they allow organizations to run applications and services in the cloud without needing to maintain physical servers themselves. Cloud computing also allows computing resources to be adjusted based on workload requirements.

### KillerCoda Linux Environment

In the KillerCoda environment, the CPU is the main compute resource. The server has an Intel Xeon E312xx processor with one CPU core, which is used to process commands and run applications.

---

## 2. Storage Resources

### Purpose

Storage resources are used to store operating system files, applications, configurations, and other data.

### Importance in Cloud Computing

Storage is important because cloud applications need a place to save and access data. Cloud storage also allows organizations to manage data without depending entirely on physical storage devices.

### KillerCoda Linux Environment

The KillerCoda server uses disk storage through devices such as `/dev/vda1`, `/dev/vda16`, and `/dev/vda15`. The main filesystem is mounted at `/`.

---

## 3. Networking Resources

### Purpose

Networking resources allow systems, servers, applications, and users to communicate with each other.

### Importance in Cloud Computing

Networking is essential in cloud computing because cloud resources need to communicate with users and other services. It also allows users to access applications and services hosted on cloud servers.

### KillerCoda Linux Environment

The KillerCoda Linux server has an IP address of `172.30.1.2`. The IP address allows the server to communicate within its network environment.

---

## 4. Operating System

### Purpose

An operating system manages computer hardware and provides an environment for applications and users.

### Importance in Cloud Computing

The operating system allows cloud servers to manage resources such as CPU, memory, storage, and networking. It also provides tools and commands for administering the server.

### KillerCoda Linux Environment

The KillerCoda server runs Ubuntu 24.04.4 LTS. The Linux terminal was used to investigate the server's hardware, storage, networking, and system information.

---

## Relationship Between the Components

Compute, storage, networking, and the operating system work together to provide a functional cloud environment. The CPU processes tasks, storage keeps data, networking enables communication, and the operating system manages the available hardware and software resources.

These components are important because a cloud server requires all of them to operate effectively. A properly configured combination of these resources allows applications and services to run reliably in a cloud environment.
