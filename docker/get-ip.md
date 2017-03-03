# Get A Container's IP Address

To get the IP address of a container, we can use `docker inspect` and automatically format the output using `--format` to get the IP.

## Use Cases
Get a container's IP:

`docker inspect --format '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $ContainerID`


Get all containers IPs:

`docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $(docker ps -a -q)`
