# Pi-Hole Installation

Runs Docker containers for Pi-Hole.

## Prerequisites

- Git

## Run with Docker Compose

1. Download the repository

   ```sh
    git clone https://github.com/devopsleigh/pihole.git
    cd pihole
    nano .env
    ```

2. Change secrets appropriately

   ```yaml
   PATH_PIHOLE=/path/on/disk
   PATH_DNSMASQ=/path/on/disk
   WEBPASSWORD=somethingsecure
   ```

  > Note: Pi-Hole web is inaccessible if the below paths are on a network share

3. Run the container

   ```sh
   docker-compose up -d --force-recreate
   ```
