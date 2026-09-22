# Checkpoint 7 - Mission Reflection

Looking back at this laboratory, moving from traditional virtual machines to containers completely changes how we build and run applications in the cloud.

First, Docker containers start up in seconds, whereas traditional virtual machines take minutes[cite: 2]. A VM has to boot a whole operating system and hardware drivers from scratch, while a container simply shares the host computer's kernel and runs only the app[cite: 2].

Second, port mapping (`-p 8080:80`) is crucial because containers operate inside a secure, isolated network box. Without forwarding the port, external users cannot access the app inside; mapping acts as a bridge, sending web traffic from port 8080 on your host computer to port 80 inside the container.

Third, using the `docker rm` command completely deletes the container along with any temporary data stored inside its writable layer. This teaches us that persistent data needs to be saved outside the container using volumes.

Additionally, containerization revolutionizes DevOps by uniting developers and IT operations. Because containers bundle the app and all its dependencies together, it fixes the old "it works on my computer" problem and guarantees the app runs identically in testing and in production.

Finally, my GitHub portfolio is growing from a simple storage space into a professional collection of cloud engineering projects. Each lab adds clear technical guides, deployment steps, and real command-line evidence, showcasing solid growth in cloud computing.
