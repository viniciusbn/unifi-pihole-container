# Pi-hole application

This repository contains a Docker Compose setup for running the Pi-hole application.

## Prerequisites
- Docker
- Docker Compose

## Getting Started

1. Clone the repository
```
gh repo clone viniciusbn/unifi-pihole-container
cd unifi-pihole-container/pihole
```
2. Create the .env file

You need to create a .env file in the root directory of the repository. This file will contain environment variables used by the Docker Compose setup. Below is a template for the .env file:
```
WEBPASSWORD="your_access_password"
VIRTUAL_HOST="your_virtual_hostname"
FTLCONF_LOCAL_IPV4="127.0.0.1"
PIHOLE_DNS_="your_external_dns_services" #Ex: "1.1.1.1;4.4.4.4"
```
Replace variables values as you needed.

3. Start the services
```
docker-compose up -d
```
This command will start the Pi-hole container in detached mode.

4. Access the Pi-hole Application

Once the containers are up and running, you can access the Pi-hole Application web interface by navigating to https://localhost/admin/login.php in your web browser.

5. Update your internal DHCP service

You need to update your internal DHCP service to use the physical IP address as a DNS service.

6. Stopping the services

To stop and remove the containers, use the following command:
```
docker-compose down
````

6. Additional Information

Ensure that the ./pihole-conf directory and its subdirectories have appropriate permissions set so that Docker can read and write data.
Modify the docker-compose.yml file if you need to customize the setup further, such as changing port mappings or resource limits.