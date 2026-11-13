# Final Reflection: Mission 1 to Mission 10

## Introduction

Completing the CCM101 -- Cloud Computing laboratory activities has given
me an opportunity to understand how cloud infrastructure works and how
different technologies are connected to build and manage a working
system. Throughout the missions, I was introduced to concepts and
practical activities involving cloud computing, Linux, containers,
infrastructure management, and automation.

Mission 10, **The Enterprise Cloud Architect**, brought these topics
together. Instead of simply following a set of instructions, I was
challenged to plan an infrastructure, make technical decisions, deploy
an application, secure the server, automate an operational task, and
document the result.

## My Learning Journey

From Mission 1 to Mission 10, I gradually developed a better
understanding of cloud computing and the tools used to manage computing
environments. The laboratory activities helped me connect theoretical
concepts with practical tasks.

I learned that setting up an environment is only one part of managing
infrastructure. A working system also needs proper configuration,
security, persistent storage, monitoring or maintenance, backup
planning, and documentation. Each part contributes to the reliability
and usability of the overall system.

The earlier missions provided the foundation that I needed for the final
activity. By the time I reached Mission 10, I had a better appreciation
of how Linux commands, virtualization, containers, networking, and
automation can work together.

## Experience in Mission 10

Mission 10 was challenging because it required independent planning and
decision-making. I had to consider the infrastructure design, the
application stack, communication between containers, and how data would
be stored.

One important lesson was the value of **Docker and Docker Compose**.
Containers make it possible to run application services in a more
organized and consistent environment. Connecting the application and
database containers also helped me understand how a multi-tier
application depends on communication between services.

I also learned why **persistent volumes** are important. Container
storage alone should not be treated as permanent data storage. A
persistent volume helps protect database data when containers are
recreated or the virtual machine is restarted.

The security requirement helped me understand the importance of
controlling network access. Configuring **UFW** with a default-deny
incoming policy and allowing only necessary ports is an important step
in reducing unnecessary exposure.

Another valuable part of the mission was automation. Creating a Bash
script and scheduling it with **Cron** showed me how repetitive
operational tasks can be performed automatically. This is useful for
tasks such as backups, log maintenance, and system health checks.

Finally, preparing the documentation helped me recognize that a
technical project should be understandable to another person. A clear
README, architecture diagram, operational manual, and source files can
help another administrator deploy, maintain, and troubleshoot the
system.

## Challenges and Lessons Learned

The final mission required me to bring several technologies together,
and this made troubleshooting an important part of the process. A
problem in networking, container configuration, permissions, storage, or
firewall rules can affect the whole application.

I learned to approach problems step by step: identify the component
involved, check its configuration and status, review relevant logs, and
test a solution before making additional changes. I also learned not to
assume that a container being in a running state automatically means the
entire application is working correctly.

The mission taught me that security and backup procedures should be
considered during the design stage rather than added only after
deployment. It also reminded me that documentation must match the actual
configuration of the system.

## Skills and Knowledge Gained

Through the laboratory activities, I improved my understanding of:

-   Cloud computing concepts and infrastructure planning.
-   Virtual machines and Ubuntu Server administration.
-   Linux commands and basic server management.
-   Docker and Docker Compose.
-   Multi-tier application deployment.
-   Container networking and persistent volumes.
-   Firewall configuration using UFW.
-   Bash scripting and Cron scheduling.
-   Backup, recovery, and operational maintenance concepts.
-   Technical documentation and infrastructure presentation.

## Conclusion

Overall, CCM101 helped me understand that cloud computing involves more
than hosting an application. It requires planning, deployment,
networking, security, storage, automation, and continuous maintenance.

Mission 10 was a meaningful final activity because it challenged me to
apply the knowledge gained from the previous missions in one integrated
project. It strengthened my confidence in working with Linux servers and
containerized applications while showing me the importance of careful
testing and documentation.

As I continue learning, I want to improve my skills in cloud
infrastructure, DevOps, server security, and automation. The experience
from these laboratory activities gives me a foundation that I can build
on in future academic projects and professional work.

------------------------------------------------------------------------

**Student:** \[Your Name\]\
**Course:** CCM101 -- Cloud Computing\
**Section:** \[Your Section\]

> **Personalize before submission:** Add specific examples of what you
> personally configured, the actual application stack you deployed,
> problems you encountered, and how you solved them. The reflection
> should accurately represent your own work and learning.

