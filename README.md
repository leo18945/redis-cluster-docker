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

## Client Access

```
    docker exec -it ${redis_container_id} redis-cli -c

    set key1 1

    set key2 2

    set key3 3

    get key1

    get key2

    get key3
```

Have fun.