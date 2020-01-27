# Pi-Hole Installation

Runs Docker containers for Pi-Hole.

## Prerequisites

- Git
- Docker macvlan network named `local`

## Run with Docker Compose

1. Download the repository

   ```sh
   git clone https://github.com/devopsleigh/pi-hole.git
   cd pi-hole
   nano .env
   ```

2. Change secrets appropriately

   ```yaml
   PATH_PIHOLE=/path/to/share
   PATH_DNSMASQ=/path/to/share
   TZ=Country/City
   IP_ADDRESS=ip.ad.dr.ess
   WEBPASSWORD=somethingsecure
   ```

3. Run the container

   ```sh
   sudo docker-compose up -d --force-recreate
   ```
