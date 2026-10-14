
# MinIO Object Storage Deployment

## Overview

This laboratory activity demonstrates how to deploy an S3-compatible object storage server using MinIO and Docker in a KillerCoda playground.

## Tools Used

- KillerCoda Ubuntu Playground
- Docker
- MinIO
- Web browser
- GitHub

## Docker Deployment Command

First, I checked the installed Docker version using:

```bash
docker --version
```

I then used the following command to deploy the MinIO server:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
chainguard/minio:latest server /data --console-address ":9001"
```

## Port Configuration

| Port | Purpose |
|---|---|
| 9000 | MinIO API endpoint |
| 9001 | MinIO Web Console |

Port 9001 is intended for accessing the MinIO Web Console through KillerCoda port forwarding.

## Environment Variables

The `-e` flag passes environment variables into the Docker container.

- `MINIO_ROOT_USER=cloudadmin` sets the configured root username.
- `MINIO_ROOT_PASSWORD=CloudNova2026!` sets the configured root password.

These variables are intended to configure the credentials used to access the MinIO service.

## Container Verification

I used the following command to check the running containers:

```bash
docker ps
```

The container should appear with the name `minio-server` and port mappings for ports 9000 and 9001.

## Bucket Creation and File Upload

The required bucket name for this activity is `client-photos`.

After confirming that the server is running, I will access the MinIO Web Console, create the bucket, and upload a sample file.

## Screenshots

- `screenshots/minio-deployed.png` — Evidence of the running MinIO container.
- `screenshots/minio-bucket-upload.png` — Evidence of the created bucket and uploaded file.

## Result

This activity practices deploying a containerized object storage service, configuring ports and environment variables, and verifying the container using Docker. The bucket creation and file upload will be completed after the MinIO Web Console is accessible.
