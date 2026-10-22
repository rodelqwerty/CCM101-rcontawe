# Laboratory 06 — Cloud Deployment Engineer

## Mission Overview

This laboratory activity demonstrates how to deploy a multi-tier cloud application using Docker Compose. The project uses Nextcloud as the web application and MariaDB as the database. Both services are defined in a YAML configuration file and deployed together.

## Objectives

- Understand two-tier application architecture.
- Create a Docker Compose YAML configuration.
- Deploy Nextcloud and MariaDB as separate containers.
- Access the Nextcloud setup page through port 8080.
- Document the deployment process and Infrastructure as Code principles.
- Maintain a GitHub portfolio with screenshots as evidence.

## Commands Executed

```bash
docker --version
docker-compose --version
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose config
docker-compose up -d
docker-compose ps
docker-compose logs --tail=100
docker-compose down
```

Note: The commands above use the standalone `docker-compose` syntax. If your environment uses the newer Docker Compose plugin, replace `docker-compose` with `docker compose`.

## Skills Learned

- Docker container management
- Docker Compose configuration
- YAML file editing and indentation
- Multi-tier application architecture
- Container networking and environment variables
- Web application deployment and verification
- Technical documentation using Markdown
- GitHub portfolio management

## Screenshots

- `screenshots/compose-deployment.png` — Deployment and container status.
- `screenshots/nextcloud-web.png` — Nextcloud installation page.
- `screenshots/compose-teardown.png` — Container teardown evidence.
