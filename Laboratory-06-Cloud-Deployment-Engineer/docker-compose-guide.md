# Docker Compose Deployment Guide

## 1. Overview

Docker Compose is a tool for defining and managing multi-container applications using a YAML configuration file. In this laboratory activity, it is used to deploy Nextcloud and MariaDB as two services in a single application stack.

## 2. Understanding the Services Block

The `services:` block defines the containers that make up the application. In this configuration, there are two services: `database` and `app`.

- **database:** Uses the `mariadb:10.6` image and defines the database credentials, database name, and database username.
- **app:** Uses the `nextcloud` image, exposes port 8080 on the host environment, and defines the database connection settings.

Docker Compose reads these definitions and manages the services together.

## 3. How Nextcloud Finds MariaDB

The environment variable `MYSQL_HOST=database` tells the Nextcloud container to use the Compose service named `database` as its database host.

Docker Compose provides service-name-based networking between containers in the same project network. This allows Nextcloud to communicate with MariaDB without requiring the database container's IP address to be manually configured.

## 4. Port Mapping

The configuration contains the following port mapping:

```yaml
ports:
  - 8080:80
```

The first port, `8080`, is the host-side port exposed by the deployment environment. The second port, `80`, is the port inside the Nextcloud container. This mapping allows browser traffic to reach the web application through the environment's port-access feature.

## 5. Environment Variables

Environment variables configure the database connection and credentials used by the services.

| Variable | Purpose |
|---|---|
| `MYSQL_ROOT_PASSWORD` | Sets the MariaDB root password during initialization |
| `MYSQL_PASSWORD` | Specifies the application database user's password |
| `MYSQL_DATABASE` | Defines the application database name |
| `MYSQL_USER` | Defines the application database username |
| `MYSQL_HOST` | Identifies the database service used by Nextcloud |

The values in this laboratory are for demonstration only. Production deployments should use stronger secret-management practices.

## 6. Docker Run vs. Docker Compose

| `docker run` | `docker-compose up -d` |
|---|---|
| Starts an individual container using command-line options | Starts and manages services defined in a Compose file |
| Requires options to be entered manually for each container | Stores service configuration in a reusable YAML file |
| Managing multiple related containers requires additional commands | Coordinates multiple related services as one application stack |

The `-d` option runs the services in the background, allowing the terminal to remain available for other commands.

## 7. Commands Used

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
cat docker-compose.yml
docker-compose config
docker-compose up -d
docker-compose ps
docker-compose logs --tail=50
docker-compose down
```

The `config` and `logs` commands are verification and troubleshooting commands. Use the equivalent `docker compose` syntax if required by the installed version.

## 8. Conclusion

Docker Compose simplifies the deployment of multi-container applications by keeping their configuration in one file. This activity demonstrates how Nextcloud and MariaDB can work together through service networking, environment variables, and port mapping.
