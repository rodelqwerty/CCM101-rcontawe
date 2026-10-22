
# Docker Compose Guide

## Introduction

Docker Compose is a tool used to define and manage applications that contain multiple Docker containers. In this laboratory activity, Docker Compose deploys Nextcloud and MariaDB using a single YAML configuration file named `docker-compose.yml`.

## What Does the `services:` Block Do?

The `services:` block defines the containers that make up the application. In this project, it contains two services: `database`, which uses the `mariadb:10.6` image, and `app`, which uses the `nextcloud` image. Each service has its own configuration, including environment variables and ports.

## How Does Nextcloud Find the Database?

Nextcloud uses the `MYSQL_HOST` environment variable to identify the database host. The value is `database`, which matches the database service name in the Compose file. Docker Compose creates a network where services can communicate using their service names.

## Difference Between `docker run` and `docker compose up -d`

The `docker run` command is commonly used to create and start an individual container with command-line options. When an application needs several connected containers, the user may have to configure their networks, environment variables, and other settings separately.

The `docker compose up -d` command reads the `docker-compose.yml` configuration and creates or starts the services defined in it. This makes a multi-container deployment easier to repeat and manage.

## Environment Variables

Environment variables provide configuration values to containers. In this project, `MYSQL_DATABASE` specifies the database name, `MYSQL_USER` specifies the database user, and `MYSQL_PASSWORD` specifies the user's password. The `MYSQL_ROOT_PASSWORD` variable configures the MariaDB root password.

## Port Mapping

The mapping `8080:80` exposes the Nextcloud web interface through port 8080 on the host and port 80 inside the container. This allows users to access Nextcloud through the KillerCoda port access feature.

## Conclusion

Docker Compose demonstrates Infrastructure as Code by storing the application configuration in a reusable YAML file. It simplifies deployment, improves consistency, and makes it easier to manage the Nextcloud application and its database together.
