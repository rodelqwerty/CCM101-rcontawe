# Mission Reflection — The Cloud Security Engineer

Completing this laboratory helped me understand why server security is important in cloud computing. A host-based firewall protects an individual server by controlling the network connections that are allowed to reach it. Even if an external network firewall is bypassed, UFW can provide another layer of protection by blocking unauthorized incoming traffic according to its rules.

Managing open network ports is also important because every exposed service can create another possible entry point for attackers. Keeping unnecessary ports closed reduces the server's attack surface. During this activity, I learned how to allow SSH for remote administration and TCP port 8080 for the web application while using a default-deny policy for incoming connections.

Leaving a database port such as MySQL port 3306 open to the public internet is dangerous because attackers may attempt password guessing, exploit vulnerabilities, or access poorly secured database services. Databases should normally be accessible only to authorized application servers and administrators. Strong authentication, restricted network access, updates, and monitoring are important parts of database security.

This mission changed my perspective because I realized that deploying an application is not enough to make a server secure. Even a working web server can be exposed to unnecessary risks if its network access is not properly configured. I also learned that firewall rules must be applied carefully, especially when managing SSH access to a remote machine.

With eight completed missions, my GitHub portfolio has become a more organized record of my cloud computing practice. It demonstrates my progress in areas such as Linux, Docker, deployment, monitoring, and security. Documenting each activity and saving screenshots also helps me review the commands I used and explain what I learned. Overall, this laboratory strengthened my understanding of defense in depth and the importance of maintaining secure configurations.

