# Checkpoint 5 - The Container Lifecycle

As a Cloud-Native Engineer, mastering container management is essential for operating reliable environments. Below is the documentation of the core Docker lifecycle commands executed in the terminal, detailing the action and practical impact of each command.

---

## Container Lifecycle Commands & Explanations

### 1. List Running Containers
* **Command:** `docker ps`
* **Explanation:** This command queries the Docker daemon to list all currently active containers, displaying essential runtime details such as container IDs, image names, port mappings, and uptime.

### 2. Stop the Running Container
* **Command:** `docker stop <container_id_or_name>`
* **Explanation:** This command gracefully sends a SIGTERM signal (followed by a SIGKILL if necessary) to the main process inside the container, safely halting its execution.

### 3. Verify It Is Stopped
* **Command:** `docker ps -a`
* **Explanation:** By passing the `-a` flag, this command lists all containers—including stopped and exited ones—allowing you to confirm that the target container's status has transitioned to "Exited".

### 4. Remove the Container Completely
* **Command:** `docker rm <container_id_or_name>`
* **Explanation:** This command permanently deletes the stopped container instance and cleans up its allocated writeable container layer from disk, freeing up system storage.

---

## 🖥️ Terminal Execution Reference

```bash
# View active containers
$ docker ps

# Stop an active container instance
$ docker stop web-app-container

# Verify container status (including stopped instances)
$ docker ps -a

# Remove the container instance from disk
$ docker rm web-app-container
