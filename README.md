# 🧪 Java Maven Build Job in Jenkins

This project demonstrates how to configure a Jenkins Freestyle job to build a simple Java application using Apache Maven. Everything is executed within a Docker-based Jenkins environment, simulating a real-world CI setup.

---

## 🎯 Objective

To automate the build process of a Java Maven project using Jenkins and validate the build success using the `mvn clean package` lifecycle.

---

## 🛠 Tools & Technologies Used

- **Jenkins** (Docker containerized)
- **Apache Maven** (v3.8.6)
- **Java JDK 8**
- **Ubuntu Linux**
- **Jenkins Freestyle Job**
- **Git** (optional for version control)
- **Local Project Directory**

---

## 📁 Project Structure

```
hello-java-maven/
├── pom.xml
└── src/
    └── main/
        └── java/
            └── HelloWorld.java
```

---

## 🧩 Setup Overview

### ✅ Java Project Creation

A basic `HelloWorld.java` file was created under the `src/main/java` directory, printing a simple greeting to the console.

A standard `pom.xml` was configured to define project metadata and include the Maven Compiler Plugin with Java 8 compatibility.

---

### ✅ Jenkins in Docker

Jenkins was deployed as a container, and the local Java Maven project directory was mounted into the container to make it accessible for the build process.

---

### ✅ Jenkins Job Configuration

A new **Freestyle Project** was created in the Jenkins dashboard with the following:

- Maven tool configured (v3.8.6)
- Build step to invoke Maven with `clean package` goals
- Path to the `pom.xml` of the mounted project directory

---

### ✅ Build Execution

The build was triggered using **Build Now** in Jenkins. Jenkins fetched the project and ran Maven to compile and package the Java application.

---

## 📸 Screenshots (Suggested)

- Jenkins build console showing `[INFO] BUILD SUCCESS`
- Freestyle job configuration page with Maven build settings
- Project folder structure inside Jenkins

---

## ✅ Outcome

Successfully automated the build of a Java Maven application using Jenkins in a Docker container. This exercise reinforced key CI/CD concepts and provided hands-on experience with:

- Maven builds via Jenkins
- Environment variable configuration
- Jenkins job setup and execution
- Dockerized CI environments

---
