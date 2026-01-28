# PahanaEDU

PahanaEDU is a multi-module Java Spring Boot application consisting of a Backend service and a Frontend web application.

## Project Structure

The project is divided into two main components:

1.  **Backend (Root)**: The core API and business logic.
    -   Type: Spring Boot Application (JAR)
    -   Location: Root directory
    -   Key Dependencies: Spring Data JPA, Spring Security, MySQL Connector, Spring Web.

2.  **Frontend**: The web interface.
    -   Type: Spring Boot Web Application (WAR)
    -   Location: `./frontend` directory
    -   Key Dependencies: Spring Web, Tomcat (provided).

## Prerequisites

-   **Java Development Kit (JDK)**: The run scripts are configured to use JDK 25 (`C:\Program Files\Eclipse Adoptium\jdk-25.0.0.36-hotspot`), but the project is configured for Java 17 compatibility. Ensure you have a compatible JDK installed.
-   **Maven**: The project includes the Maven Wrapper (`mvnw`), so a local Maven installation is not strictly required.

## Configuration

Configuration settings (database connections, server ports, etc.) can be found in:

-   **Backend**: `src/main/resources/application.properties`
-   **Frontend**: `frontend/src/main/resources/application.properties`

## Running the Application

PowerShell scripts are provided to easily start both services.

### 1. Start the Backend

Open a PowerShell terminal in the root directory and run:

```powershell
.\run_backend.ps1
```

This script sets the `JAVA_HOME` environment variable and runs the Spring Boot application using the Maven wrapper.

### 2. Start the Frontend

Open a new PowerShell terminal in the root directory and run:

```powershell
.\run_frontend.ps1
```

This script navigates to the `frontend` directory and starts the frontend application.

## Notes

-   Ensure your MySQL database is running and configured according to the settings in the backend's `application.properties` before starting the application.
-   The run scripts currently point to a specific JDK path. You may need to edit `run_backend.ps1` and `run_frontend.ps1` if your JDK is located elsewhere.
