# Checkpoint 6 - Technical Documentation
---
# Laboratory 4: Mission 4 - The Cloud-Native Engineer
---
## Mission Overview

Congratulations on your promotion to the Cloud-Native Engineering Team at CloudNova Technologies[cite: 3]. Modern cloud computing has evolved beyond traditional Virtual Machines (VMs) toward lightweight, portable, and lightning-fast Containers[cite: 3]. This laboratory activity bridges the gap between virtualization and containerization using the KillerCoda Playground, allowing you to execute fundamental Docker CLI commands, deploy a live Nginx web server, and manage container lifecycles like a professional Cloud-Native Engineer[cite: 3].

*Evidence:* ![Checkpoint 1](screenshots/Checkpoint%201%20-%20Expand%20Your%20Cloud%20Portfolio.png)

---

## Objectives

By completing this laboratory activity, the following objectives were achieved:
* Differentiate between traditional Virtual Machines (VMs) and Containers[cite: 3].
* Access a Docker-enabled cloud environment using KillerCoda[cite: 3].
* Execute fundamental Docker CLI (Command Line Interface) commands[cite: 3].
* Pull, run, manage, and terminate a containerized Nginx application[cite: 3].
* Create professional technical documentation of container operations using Markdown[cite: 3].
* Continue developing a well-organized GitHub Cloud Computing Portfolio[cite: 3].

*Evidence:* ![Checkpoint 2](screenshots/Checkpoint%202%20-%20Research%20Virtual%20Machines%20vs.%20Containers%20.png)

---

## Docker Commands Executed (Reference Table)

The table below outlines all the core Docker commands executed across Checkpoints 3, 4, and 5, detailing their functions and corresponding visual evidence.

| Checkpoint | Command | Description / Action | Terminal Evidence |
| :--- | :--- | :--- | :--- |
| **Checkpoint 3** | `docker --version`<br>`docker info` | Verifies that Docker is installed and displays system-wide daemon status[cite: 3]. | ![Checkpoint 3](screenshots/Checkpoint%203%20-%20docker-version.png) |
| **Checkpoint 4** | `docker pull nginx`<br>`docker run -d -p 8080:80 --name web-app-container nginx`<br>`curl http://localhost:8080` | Downloads the Nginx image, runs it in detached mode mapping port 8080, and verifies local HTTP output[cite: 3]. | ![Checkpoint 4](screenshots/Checkpoint%204%20-%20nginx-running.png) |
| **Checkpoint 5** | `docker ps`<br>`docker stop web-app-container`<br>`docker ps -a`<br>`docker rm web-app-container` | Lists, stops, verifies, and permanently removes the running container from disk[cite: 3]. | ![Checkpoint 5](screenshots/Checkpoint%205%20-%20container-lifecycle.png) |

*Deployment Evidence:* ![Checkpoint 5.1](screenshots/Checkpoint%205.1%20-%20container-lifecycle.png)

---

## Skills Learned

* **Container Architecture Fundamentals:** Understood how containers share a host OS kernel to eliminate hardware-level virtualization bloat.
* **CLI Operational Mastery:** Gained hands-on experience navigating the Docker command-line interface to pull images, manage port bindings, and trace container states.
* **Lifecycle Administration:** Learned how to safely initialize, monitor, interrupt, and prune container resources.
* **Technical Engineering Documentation:** Developed clean, standardized Markdown reports tailored for client implementation and team handoffs.

*Documentation Evidence:* ![Checkpoint 6](screenshots/Checkpoint%206%20-%20Technical%20Documentation.png)

---

## Challenges Encountered

* **Port Mapping Logic:** Balancing external host ports with internal container ports (e.g., `-p 8080:80`) required careful attention to syntax to prevent routing conflicts.
* **Container State Tracking:** Learning the nuance between active processes (`docker ps`) and terminated instances (`docker ps -a`) during lifecycle management checks.

*Reflection Evidence:* ![Checkpoint 7](screenshots/Checkpoint%207%20-%20Mission%20Reflection%20.png)
