# Hello World Java App with Docker and Docker Compose

## Overview

This project demonstrates how to containerize a simple Java "Hello World" application using Docker. It includes two versions:

* A standalone Dockerized Java app.
* A Docker Compose setup for container orchestration.

## Folder Structure

```
hello_world_dockerfile/      # Standalone Docker setup
  |- Dockerfile              # Dockerfile to build the Java app image
  |- pom.xml                 # Maven build file
  |- src/                    # Java source code
  |- target/                 # Compiled output

docker-compose/              # Docker Compose version
  |- docker-compose.yml      # Defines service(s) and image build
  |- Dockerfile              # Dockerfile to build the Java app image
  |- pom.xml, src/, target/  # Same as above
```

## Prerequisites

* [Docker](https://www.docker.com/products/docker-desktop)
* [Docker Compose](https://docs.docker.com/compose/) (only for compose version)
* [Java JDK 8+](https://www.oracle.com/java/technologies/javase-downloads.html)
* [Maven](https://maven.apache.org/)

## Running the App (Standalone Docker)

1. Navigate to the folder:

   ```bash
   cd hello_world_dockerfile
   ```
2. Build the Maven project:

   ```bash
   mvn clean package
   ```
3. Build the Docker image:

   ```bash
   docker build -t hello-world-java .
   ```
4. Run the Docker container:

   ```bash
   docker run --rm hello-world-java
   ```

## Running with Docker Compose

1. Navigate to the folder:

   ```bash
   cd docker-compose
   ```
2. Build and start the services:

   ```bash
   docker-compose up --build
   ```
3. To stop:

   ```bash
   docker-compose down
   ```

## Output

You should see something like:

```
Hello, World from Java!
```

## License

This project is for educational purposes.

---

Feel free to customize the app further or integrate with other services using Docker Compose!
