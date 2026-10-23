# Laboratory 06 — The Cloud Deployment Engineer

**Course:** CCM101 – Cloud Computing  
**Mission:** Mission 6 — The Cloud Deployment Engineer

## Mission Overview

This laboratory activity demonstrates how to deploy a multi-tier cloud application using Docker Compose. The application consists of Nextcloud as the web/application tier and MariaDB as the database tier.

The deployment is defined in a `docker-compose.yml` file and managed through the Linux command line in a KillerCoda playground.

## Objectives

- Explain the purpose of a two-tier application architecture.
- Create a Docker Compose configuration using YAML.
- Deploy Nextcloud and MariaDB as separate containers.
- Verify the deployment and access Nextcloud through a browser.
- Shut down the application stack using Docker Compose.
- Document the process and provide screenshot evidence.

## Architecture

| Service | Technology | Responsibility |
|---|---|---|
| Application | Nextcloud | Provides the web interface and cloud storage application |
| Database | MariaDB 10.6 | Stores application data |
| Orchestration | Docker Compose | Defines and manages the services |

## Commands Executed

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

## Screenshots

Deployment and browser evidence are stored in the `screenshots/` directory.

- `compose-deployment.png` — deployment and running containers.
- `nextcloud-web.png` — Nextcloud initial setup page.
- `compose-teardown.png` — stopped and removed containers.

## Skills Learned

- Understanding multi-tier architecture.
- Writing and checking YAML configuration files.
- Using Docker Compose to manage multiple containers.
- Configuring application-to-database communication.
- Accessing containerized applications through port mapping.
- Troubleshooting deployments and documenting technical work in Markdown.

## Related Documentation

- [Two-Tier Architecture](multi-tier-architecture.md)
- [Docker Compose Deployment Guide](docker-compose-guide.md)
- [Mission Reflection](reflection.md)

## Conclusion

This activity provided practical experience in defining, deploying, verifying, and removing a multi-container application. It also demonstrated how Infrastructure as Code makes cloud deployment procedures more organized and repeatable.
