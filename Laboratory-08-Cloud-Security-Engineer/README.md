# Laboratory 08 — The Cloud Security Engineer

## Mission Overview

This laboratory focuses on securing an Ubuntu server using the Uncomplicated Firewall (UFW). An Nginx web application is deployed in Docker, and firewall rules are configured to allow necessary services while blocking unauthorized incoming traffic by default.

## Objectives

- Understand the Principle of Least Privilege.
- Explain the concept of an attack surface.
- Deploy an Nginx container named `secure-web-app`.
- Configure UFW with a default-deny incoming policy.
- Allow SSH and TCP port 8080.
- Verify firewall rules and document the security configuration.
- Maintain evidence and documentation in the GitHub portfolio.

## Commands Executed

| Command | Purpose |
|---|---|
| `docker --version` | Check the Docker version |
| `docker ps` | Inspect running containers |
| `docker run -d --name secure-web-app -p 8080:80 nginx` | Deploy the Nginx container |
| `curl -i http://localhost:8080/` | Test the web application |
| `sudo ufw allow ssh` | Permit SSH access |
| `sudo ufw default deny incoming` | Block incoming traffic by default |
| `sudo ufw default allow outgoing` | Permit outgoing traffic by default |
| `sudo ufw enable` | Activate UFW |
| `sudo ufw status verbose` | Inspect firewall status and policies |
| `sudo ufw allow 8080/tcp` | Permit TCP traffic on port 8080 |
| `sudo ufw status numbered` | Display numbered firewall rules |

## Skills Learned

- Basic Linux server administration.
- Docker container deployment.
- Firewall configuration with UFW.
- Network port management.
- Security documentation using Markdown.
- Version control and evidence management using Git and GitHub.

## Evidence

Screenshots for the deployment and firewall configuration are stored in the `screenshots/` directory.

## Conclusion

This mission demonstrates how a host-based firewall can reduce a server's attack surface by restricting incoming connections to the services that are required.
