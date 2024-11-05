## Agile Software Practice - Assignment 1.

__Name:__ Junwei Liu

__Demo:__ 

This repository contains the containerization of the mukti-container application illustrated below.

![](./images/arch.png)

### Database Seeding.
To automate database seeding, I added a seeder service in Docker Compose that connects to MongoDB using the MONGODB_URI environment variable. Built from a dedicated Dockerfile (Dockerfile-seeder), this service runs seeding scripts automatically at startup and is configured to run only once, stopping after completion. This setup ensures consistent data initialization across development and production environments.

### M.ulti-Stack.
To manage both development and production environments, the Docker setup uses docker-compose.override.yml for development-specific configurations and docker-compose.prod.yml for production settings, along with the base docker-compose.yml. This allows for easy switching between environments while keeping core service definitions consistent.