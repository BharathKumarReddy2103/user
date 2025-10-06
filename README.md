# Roboshop User Microservice CI

Welcome to the **User Microservice** of the **Roboshop Application**, a microservices-based e-commerce platform for selling robots. This repository contains the code and CI configuration for the user service, a core component responsible for user registration, authentication, and management.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [CI Pipeline](#ci-pipeline)
- [Jenkins Shared Library](#jenkins-shared-library)
- [Dockerization](#dockerization)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

The **User Microservice** handles all user-related operations such as registration, authentication, and user data management. It is designed to be scalable, maintainable, and easily deployable as part of the Roboshop microservices ecosystem.

---

## Features

- User registration and authentication (login/logout)
- JWT-based security
- RESTful API endpoints
- Integration with other Roboshop microservices
- Containerized with Docker
- Automated CI/CD with Jenkins
- Utilizes a custom [Jenkins Shared Library](https://github.com/BharathKumarReddy2103/jenkins-shared-library) for pipeline reusability

---

## Tech Stack

- **Programming Language:** Java
- **Authentication:** JWT
- **Containerization:** Docker
- **CI/CD:** Jenkins

---

## Architecture

The User Microservice is part of a distributed system, communicating with other services via REST APIs or message queues. It focuses solely on user domain logic, following the principles of microservices architecture.

```
[Client] <---> [API Gateway] <---> [User Service]
                                    |
                                    +--> [Database]
```

---

## Getting Started

### Prerequisites

- Docker
- Jenkins (for CI)
- (Add language/runtime prerequisites, e.g. Node.js, Python, etc.)

### Clone the repository

```bash
git clone https://github.com/BharathKumarReddy2103/user.git
cd user
```

### Environment Setup

1. Copy `.env.example` to `.env` and update variables as needed.
2. Install dependencies:

   ```bash
   # Example for Node.js
   npm install
   ```

### Running Locally

```bash
# Example for Node.js
npm start
```
*Replace with your project’s local run command.*

---

## CI Pipeline

This repository includes a `Jenkinsfile` for automated build, test, and deployment processes. The pipeline leverages a [Jenkins Shared Library](https://github.com/BharathKumarReddy2103/jenkins-shared-library) for standardized pipeline steps such as linting, testing, building Docker images, and deployment.

---

## Jenkins Shared Library

The custom [Jenkins Shared Library](https://github.com/BharathKumarReddy2103/jenkins-shared-library) is used to:

- Centralize and reuse pipeline logic across Roboshop microservices
- Enforce consistent quality gates
- Simplify maintenance of CI/CD processes

---

## Dockerization

A `Dockerfile` is provided for building container images:

```bash
docker build -t roboshop-user-service .
docker run -p 8080:8080 --env-file .env roboshop-user-service
```

---

## Contributing

Contributions are welcome. Please open issues or pull requests for any changes, improvements, or bug fixes.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
