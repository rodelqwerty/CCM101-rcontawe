# Mission Reflection

This laboratory activity helped me understand how Docker Compose can make cloud deployment easier and more organized. Before completing this activity, I understood that Docker containers could run applications individually. However, I learned that real-world applications often need multiple services to work together, such as a web application and a database.

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because the configurations for multiple containers are stored in one file. Instead of manually starting and configuring each container, I can use a single command to deploy the entire application. This also makes the deployment easier to repeat and maintain.

I also learned that YAML indentation is very important. If I use incorrect spacing or tabs instead of spaces, Docker Compose may fail to read the configuration. This can prevent the containers from starting properly. Because of this, I need to carefully check the structure and indentation of my configuration file.

Environment variables are useful because they allow containers to receive the configuration values they need. In this activity, the MariaDB container uses environment variables to configure the database, username, and passwords. The Nextcloud container uses matching database settings and the `MYSQL_HOST` variable to connect to the database service.

Deploying Nextcloud with MariaDB helped me see how different services can work together to provide a private cloud storage application. I also learned how to check container status, access a web interface through a mapped port, and stop the application when testing is finished.

Since Mission 1, my understanding of Cloud Computing has improved. I now recognize that cloud computing involves more than running applications; it also requires planning, configuration, networking, and documentation. Overall, this activity improved my confidence in using Docker Compose and helped me understand the importance of Infrastructure as Code in modern cloud deployment.

