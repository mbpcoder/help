tipe: we can have a lot of containers base on an image

run a docker image. it download image if not present in local
```bash
sudo docker run hello-world 
```

list all docker images
```bash
sudo docker images
```

show all previously run container
```bash
sudo docker ps -a
```

download a docker image from hub.docker.com
```bash
sudo docker pull hello-world
```

run a docker image and then run the echo command from the created container
```bash
sudo docker run busybox echo "Hello from busybox"
```

Send stop signal to busybox container and wait for 30 seconds then if it still running kill the process
```bash
docker stop --time=30 busybox
```

remove previously created container by it is number (648795252)
```bash
sudo docker rm 648795252
```

remove docker image by it is name
```bash
sudo docker rmi hello-world
```

remove all previously created docker containers
```bash
sudo docker container prune
```

This will remove:
  - all stopped containers
  - all networks not used by at least one container
  - all images without at least one container associated to them
  - all build cache
```bash
sudo docker system prune -a
```

run docker image and after it finished remove the container
```bash
sudo docker run --rm hello-world
```

Run docker image and give me the interactive shell inside the container
```bash
sudo docker run -it hello-world
```

Give me the interactive shell inside the container with bash
```bash
docker exec -it hello-world bash
```

Execute a command in a running container
```bash
sudo docker exec 648795252 touch "/hi"
```

Run the Redis image and map port 6379 on the container to 100 in the host OS
```bash
sudo docker run -p100:6379 redis
```

create a name for container to access it without it's number
```bash
sudo docker run --name hello hello-world
```

run image in background (daemon)
```bash
sudo docker run -d hello-world
```

Map /data in container to /tmp/data in host os, this way we can create persistent storage for redis
```bash
sudo docker run redis -v /tmp/data/redis:/data
```

Create an image from a docker file in current directory
```bash
sudo docker build .
```

Build image and add tag, version to it
```bash
sudo docker build -t myapp:v1 .
```

Show already created docker network
```bash
sudo docker network ls
```

create a network with mynet name
```bash
sudo docker network create mynetwork
```

run a docker image and use mynet network this way running docker container can access other containers with thir name
```bash
docker run redis --network mynet
```

Debug docker containers
```bash
docker logs <container_id>
```

Debug docker containers and tail -f
```bash
docker logs <container_id> -f
```


