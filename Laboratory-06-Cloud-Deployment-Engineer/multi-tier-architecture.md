
# Checkpoint 2 – Research: Multi-Tier Architecture

## 1. Introduction

A **Two-Tier Architecture** is a software design that separates an application into two main components: the **Web/Application Tier** and the **Database Tier**. Each tier has a specific responsibility, and they communicate with each other to make the application work properly.

In this project, **Nextcloud** serves as the web application, while **MariaDB** serves as the database. Both services run in separate Docker containers and work together to provide a private cloud storage system.

## 2. The Web/Application Tier

The **Web/Application Tier** is responsible for providing the user interface, processing user requests, and managing the application's main functions.

In this project, Nextcloud runs inside a Docker container and allows users to access their files through a web browser. It handles user interactions, file uploads and downloads, and requests to retrieve or update information stored in the database.

**Main responsibilities:**
- Display the Nextcloud interface in a web browser.
- Handle HTTP requests from users.
- Manage file uploads, downloads, and file organization.
- Communicate with the database to retrieve and update information.
- Provide access to cloud storage features.

## 3. The Database Tier

The **Database Tier** is responsible for storing, organizing, retrieving, and managing the persistent data required by the application.

In this project, MariaDB runs inside a separate Docker container and stores the database records used by Nextcloud. These records include user account information, application settings, and file metadata. The actual uploaded files are stored separately from the database, depending on the Nextcloud storage configuration.

**Main responsibilities:**
- Store user account and application information.
- Maintain file metadata and other database records.
- Retrieve and update data when requested by Nextcloud.
- Keep application data organized and consistent.
- Provide persistent data storage.

## 4. Why Separate Them?

Separating the web application and database into two containers makes the system easier to maintain, troubleshoot, and manage. Each container can be configured, updated, or scaled independently without requiring changes to the other service. This separation also helps isolate responsibilities and allows Docker Compose to manage the containers and their network communication as one application stack.

## 5. How the Two Tiers Work Together

The two tiers communicate to process user requests and retrieve the required information.

1. The user opens Nextcloud using a web browser.
2. The Nextcloud application receives and processes the user's request.
3. If database information is needed, Nextcloud sends a request to MariaDB.
4. MariaDB retrieves or updates the requested database records.
5. Nextcloud processes the result and displays the appropriate response to the user.

**Architecture Overview:**

```text
+------------------------------+
|          USER                |
|        Web Browser           |
+------------------------------+
               |
               | HTTP/HTTPS
               v
+------------------------------+
|    WEB/APPLICATION TIER      |
|                              |
|    Nextcloud Container       |
|                              |
| - User Interface             |
| - File Management            |
| - Request Processing         |
+------------------------------+
               |
               | Database Connection
               v
+------------------------------+
|       DATABASE TIER          |
|                              |
|     MariaDB Container        |
|                              |
| - User Records               |
| - Application Settings       |
| - File Metadata              |
+------------------------------+
```

## 6. Conclusion

A two-tier architecture separates an application into a web/application tier and a database tier, with each tier performing a different role. In this project, Nextcloud provides the cloud storage interface and handles user requests, while MariaDB stores and manages the application's database records. Using separate Docker containers improves maintainability, organization, and flexibility while demonstrating the basic principles of containerized application deployment.
