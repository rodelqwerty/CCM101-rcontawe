# Mission Reflection

This laboratory activity helped me understand why monitoring is an important part of cloud computing. Before deploying an application, it is necessary to check the host server's resources, including RAM, disk capacity, and CPU usage. Even when containers are running correctly, limited host resources can affect their performance and cause applications to become slow or unavailable.

I learned that the `docker logs` command is useful when troubleshooting application problems. For example, if a user cannot access a web page, the logs can help identify failed requests, HTTP error codes, and other recorded events. Instead of guessing what happened, an engineer can use this information to investigate the problem.

I also learned the difference between logs and metrics. Logs record individual events and requests, while metrics provide numerical information about system performance. In this activity, I used application logs to identify the intentional 404 error and Docker Stats to observe the container's CPU and memory consumption. Both are important because logs help explain events, while metrics help reveal resource usage and possible performance issues.

Large enterprise companies may operate thousands of containers, making manual monitoring difficult. They can use monitoring platforms such as Prometheus to collect metrics and Grafana to visualize performance through dashboards and alerts. These tools help operations teams identify unusual resource consumption and investigate problems across many services.

Overall, this laboratory activity improved my ability to troubleshoot Linux environments. I practiced checking system resources, deploying an Nginx container, generating HTTP requests, finding errors in application logs, and monitoring container metrics. I now understand that deploying an application is only one part of cloud operations. Engineers must also continuously observe system health, investigate issues using evidence, and ensure that applications remain reliable and available to users.

