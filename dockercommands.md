# build the docker image

docker build -t jsonserverimage .

# run container from the image

docker container run -d -p 8080:8080 --name jsonserver jsonserverimage

# check the running docker containers

docker ps -a

# check the logs of jsonserver

docker logs jsonserver

# access jsonserver from the host/EC2 instance

curl 0.0.0.0:8080

# clean up

docker stop jsonserver
docker rm jsonserver
