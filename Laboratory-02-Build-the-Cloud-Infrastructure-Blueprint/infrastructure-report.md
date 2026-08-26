# Infrastructure Report

## Operating System

| Information      | Details            |
| ---------------- | ------------------ |
| Operating System | Ubuntu 24.04.4 LTS |

## Kernel Version

| Information    | Details           |
| -------------- | ----------------- |
| Kernel Version | 6.8.0-138-generic |

## CPU Information

| CPU Information     | Details                                       |
| ------------------- | --------------------------------------------- |
| Architecture        | x86_64                                        |
| CPU Operation Modes | 32-bit, 64-bit                                |
| Address Sizes       | 39 bits physical, 48 bits virtual             |
| Byte Order          | Little Endian                                 |
| CPU(s)              | 1                                             |
| Online CPU(s)       | 0                                             |
| Vendor ID           | GenuineIntel                                  |
| Model Name          | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| BIOS Vendor ID      | Red Hat                                       |
| BIOS Model Name     | RHEL-9.6.0 PC (Q35 + ICH9, 2009) CPU @ 2.0GHz |
| BIOS CPU Family     | 1                                             |
| CPU Family          | 6                                             |
| Model               | 42                                            |
| Threads per Core    | 1                                             |
| Cores per Socket    | 1                                             |
| Sockets             | 1                                             |
| Stepping            | 1                                             |
| BogoMIPS            | 7008.00                                       |
| Hypervisor Vendor   | KVM                                           |
| Virtualization Type | Full                                          |
| L1d Cache           | 32 KiB                                        |
| L1i Cache           | 32 KiB                                        |
| L2 Cache            | 4 MiB                                         |
| L3 Cache            | 16 MiB                                        |
| NUMA Nodes          | 1                                             |
| NUMA Node 0 CPU(s)  | 0                                             |

## Memory

| Memory Type |   Total |    Used |    Free |  Shared | Buff/Cache | Available |
| ----------- | ------: | ------: | ------: | ------: | ---------: | --------: |
| RAM         | 1.9 GiB | 419 MiB | 861 MiB | 1.1 MiB |    789 MiB |   1.4 GiB |
| Swap        | 1.0 GiB |     0 B | 1.0 GiB |       — |          — |   1.0 GiB |

## Storage and Mounted File Systems

### Disk Capacity

| Filesystem | Size | Used | Available | Use% | Mounted On |
| ---------- | ---: | ---: | --------: | ---: | ---------- |
| tmpfs      | 191M | 996K |      190M |   1% | /run       |
| /dev/vda1  |  19G | 5.4G |       13G |  30% | /          |
| tmpfs      | 952M |  84K |      952M |   1% | /dev/shm   |
| tmpfs      | 5.0M |    0 |      5.0M |   0% | /run/lock  |
| /dev/vda16 | 881M | 117M |      703M |  15% | /boot      |
| /dev/vda15 | 105M | 6.2M |       99M |   6% | /boot/efi  |

### Mounted File Systems

| Target                     | Source       | File System Type |
| -------------------------- | ------------ | ---------------- |
| `/`                        | `/dev/vda1`  | ext4             |
| `/sys`                     | sysfs        | sysfs            |
| `/sys/kernel/security`     | securityfs   | securityfs       |
| `/sys/fs/cgroup`           | cgroup2      | cgroup2          |
| `/sys/fs/pstore`           | pstore       | pstore           |
| `/sys/fs/bpf`              | bpf          | bpf              |
| `/sys/kernel/debug`        | debugfs      | debugfs          |
| `/sys/kernel/tracing`      | tracefs      | tracefs          |
| `/sys/fs/fuse/connections` | fusectl      | fusectl          |
| `/sys/kernel/config`       | configfs     | configfs         |
| `/proc`                    | proc         | proc             |
| `/proc/sys/fs/binfmt_misc` | systemd-1    | autofs           |
| `/dev`                     | udev         | devtmpfs         |
| `/dev/pts`                 | devpts       | devpts           |
| `/dev/shm`                 | tmpfs        | tmpfs            |
| `/dev/hugepages`           | hugetlbfs    | hugetlbfs        |
| `/dev/mqueue`              | mqueue       | mqueue           |
| `/run`                     | tmpfs        | tmpfs            |
| `/run/lock`                | tmpfs        | tmpfs            |
| `/boot`                    | `/dev/vda16` | ext4             |
| `/boot/efi`                | `/dev/vda15` | vfat             |

## Hostname

| Information | Details |
| ----------- | ------- |
| Hostname    | ubuntu  |

## IP Address

| Information           | Details    |
| --------------------- | ---------- |
| Primary IP Address    | 172.30.1.2 |
| Additional IP Address | 172.17.0.1 |

## Linux Commands Used

```bash
cat /etc/os-release
uname -r
lscpu
nproc
free -h
df -h
findmnt
hostname
hostname -I
```


