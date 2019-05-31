# Deploy Redis Cluster by Docker-compose

Redis Cluster via Docker Compose with --scale capability using Redis 5's cluster support. 

## Requirements

Docker and Docker Compose installed.

## Usage

Choose a number of nodes for the cluster (at least 6)

**Launch cluster**
```
    docker-compose up -d --scale redis=6
    docker-compose logs -f
```
It takes a little while.
    
**Stop containers**

```
    docker-compose down -v
```