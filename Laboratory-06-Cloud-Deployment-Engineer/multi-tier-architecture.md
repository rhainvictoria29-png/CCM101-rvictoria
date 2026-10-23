# Two-Tier Architecture

## Overview

A two-tier architecture is a system design that separates an application into two main parts: the web/application tier and the database tier. In this laboratory activity, Nextcloud serves as the web application, while MariaDB stores the database information required by Nextcloud.

## 1. Web/Application Tier

The web/application tier handles user interactions and provides the interface that users access through a web browser. In this deployment, Nextcloud runs inside a Docker container and receives HTTP requests through port 8080, which is mapped to port 80 inside the container.

**Main responsibilities:**
- Display the Nextcloud web interface.
- Process requests from users.
- Communicate with the database tier.
- Provide private cloud storage functionality.

## 2. Database Tier

The database tier stores and manages the information needed by the application. In this laboratory activity, MariaDB runs in a separate Docker container and uses the database name `nextcloud_db`.

**Main responsibilities:**
- Store application data and account-related information.
- Organize and manage database records.
- Respond to database requests from Nextcloud.
- Maintain persistent information required by the application.

## 3. Why Separate the Tiers?

Separating the web application and database into different containers makes the system easier to manage, maintain, and troubleshoot. Each service can be configured and updated independently, while Docker Compose helps coordinate the containers. This separation also provides a clearer structure for expanding the application in the future.

## 4. Architecture Summary

| Component | Technology | Purpose |
|---|---|---|
| Web/Application Tier | Nextcloud | Provides the web interface and cloud storage application |
| Database Tier | MariaDB | Stores and manages application data |
| Container Orchestration | Docker Compose | Defines and manages both services |
| Access Port | 8080 | Allows browser access to Nextcloud through the host environment |

## Conclusion

The two-tier architecture provides a structured way to deploy an application and its database as separate services. Using Nextcloud, MariaDB, and Docker Compose demonstrates how multiple containers can work together as one application stack.
