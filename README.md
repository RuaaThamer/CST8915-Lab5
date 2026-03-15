# CST8915 - Lab 5: Dockerization and Microservices
**Name:** Ruaa Thamer  
**Student ID:** 040819157  
**Program:** Cloud Development and Operations

## Demo Video
[View the Lab 5 Demo on YouTube](https://youtu.be/0YP4hi6HEVg)

## Project Overview
This lab demonstrates the containerization of a microservices-based application (Algonquin Pet Store). It involves creating Dockerfiles for Node.js and Python services, orchestrating them with Docker Compose, and pushing the final images to Docker Hub.

## Docker Hub Repositories
The images used in this project are hosted on Docker Hub:
- [ruaathamer/order-service](https://hub.docker.com/r/ruaathamer/order-service)
- [ruaathamer/product-service](https://hub.docker.com/r/ruaathamer/product-service)
- [ruaathamer/store-front](https://hub.docker.com/r/ruaathamer/store-front)

## Setup Challenges & Lessons Learned
During the deployment of the `store-front` container, I encountered an error where Port 80 was already in use by Windows system services. 

**Solution:** I modified the `docker-compose.yaml` to map the host port **8080** to the container port **80**. This allowed the application to run successfully without requiring administrative changes to the host OS.

## How to Run the Application
1. Ensure Docker Desktop is installed and running.
2. Download the `docker-compose.yaml` file from this repository.
3. Open a terminal in the folder containing the file and run:
   ```bash
   docker compose up
