# Redis Docker Setup

This repository contains the configuration to run a Redis server using Docker.

## Prerequisites

- Docker installed on your system. You can download and install Docker from [here](https://docs.docker.com/get-docker/).

## Getting Started

1. **Clone the repository**

   ```sh
   git clone https://github.com/kahnu044/redis-docker
   cd redis-docker
   ```

2. Run the Docker Compose

   ```bash
   docker-compose up -d
   ```

   This command will start the Redis server in detached mode.

3. Verify the setup

   To verify that the Redis server is running, you can use the following command:

   ```bash
   docker ps
   ```

   You should see a container named redis-server running.

### Services

- redis-server: The Redis server, exposed on port 6379.

### Volumes

- redis-data: A Docker volume to persist Redis data.

### Connecting to Redis

You can connect to the Redis server using any Redis client. The server is accessible at localhost:6379.

For example, using the Redis CLI:

```bash
redis-cli -h localhost -p 6379
```

### Stopping the Services

To stop the services, run:

```bash
docker-compose down
```

This will stop and remove the containers defined in the docker-compose.yml file.

### Cleaning Up

To remove the Docker volume and clean up any persistent data:

```bash
docker-compose down -v
```

## Author

[Kahnu Charan Swain](https://github.com/kahnu044)
