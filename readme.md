# Demo Project: Server Setup and Application Deployment on DigitalOcean

## Project Overview
This project demonstrates my ability to set up and configure a server on **DigitalOcean**, implement best practices for server security, and deploy a Java application using **Gradle**. The goal was to create a robust environment to host and run applications efficiently.

---

## Technologies Used
- **DigitalOcean**: Cloud platform for deploying and managing virtual private servers (Droplets).
- **Linux**: Operating system for server configuration and application hosting.
- **Java**: Programming language for the application.
- **Gradle**: Build automation tool for Java applications.

---

## Project Description

### 1. **Server Setup on DigitalOcean**
- Provisioned a new Droplet on DigitalOcean with a Linux operating system.
- Configured Droplet settings, including SSH key-based authentication for secure access.

### 2. **Security Configuration**
- Created and configured a new Linux user with limited privileges (non-root user).
- Set up a strong password policy and enforced security best practices:
  - Disabled root login.
  - Configured a firewall to allow only necessary ports (e.g., SSH and application-specific ports).

### 3. **Application Deployment**
- Installed Java runtime and Gradle on the server to support the Java application.
- Cloned the application source code from the repository.
- Built the application using Gradle (`gradle build`).
- Deployed the built application to run on the server:
  - Configured the application to run in the background as a service.
  - Verified successful deployment by testing application endpoints.

---

## Key Deliverables
1. **DigitalOcean Droplet**:
   - Securely set up and configured for application hosting.
2. **Linux User Configuration**:
   - Created a non-root user and applied security best practices.
3. **Deployed Java Application**:
   - Successfully built and deployed the Gradle application to the server.

---

## How to Reproduce This Setup

### Prerequisites
- A DigitalOcean account.
- SSH key pair for secure server access.
- Application source code compatible with Gradle.

### Steps
1. **Create a Droplet**:
   - Log in to your DigitalOcean account and create a new Droplet with a Linux distribution (e.g., Ubuntu 22.04).

2. **Set Up SSH Access**:
   - Add your public SSH key to the Droplet for secure access.
   - Connect to the Droplet using `ssh username@server_ip`.

3. **Configure Server Security**:
   - Create a new Linux user: `sudo adduser newuser`.
   - Grant limited privileges to the user: `sudo usermod -aG sudo newuser`.
   - Set up a firewall

4. **Install Java and Gradle**:
   - Install Java: `sudo apt update && sudo apt install default-jdk`

5. **Deploy the Application**:
   - Clone the application code: `git clone <repository_url>`.
   - Navigate to the project directory and build: `gradle build`.
   - Run the application using `java -jar` or configure it as a service.
