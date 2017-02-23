# Stop & Remove All Containers

You can list all Docker containers with `docker ps -a` along with the `-q` option to return only IDs. Combine this with `docker stop` and `docker rm` to stop and remove all containers at once.

## Use Cases
To stop all containers:

`docker stop $(docker ps -a -q)`

To remove all containers:

`docker rm $(docker ps -a -q)`
