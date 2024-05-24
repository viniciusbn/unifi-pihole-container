#Unifi Network Application with MongoDB

This repository contains a Docker Compose setup for running the Unifi Network Application with a MongoDB backend.

Prerequisites
Docker
Docker Compose
Getting Started
1. Clone the repository
```
gh repo clone viniciusbn/unifi-pihole-container
cd unifi-pihole-container
```
2. Create the .env file
You need to create a .env file in the root directory of the repository. This file will contain environment variables used by the Docker Compose setup. Below is a template for the .env file:
```
MONGO_USER=your_mongo_username
MONGO_PASS=your_mongo_password
MONGO_HOST=unifi-db
MONGO_DBNAME=unifi
```
Replace your_mongo_username, your_mongo_password, and unifi with your desired MongoDB username, password, and database name respectively.

3. Start the services
```
docker-compose up -d
```
This command will start the MongoDB and Unifi Network Application containers in detached mode.

4. Access the Unifi Network Application
Once the containers are up and running, you can access the Unifi Network Application web interface by navigating to https://localhost:8443 in your web browser.

Stopping the services
To stop and remove the containers, use the following command:
```
docker-compose down
````

Additional Information
Ensure that the ./unifi-conf directory and its subdirectories have appropriate permissions set so that Docker can read and write data.
Modify the docker-compose.yml file if you need to customize the setup further, such as changing port mappings or resource limits.