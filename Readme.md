# GET CONTAINERS

docker ps
docker ps -a

# STOP & REMOVE CONTAINER

docker stop [containerId]
docker rm [containerId]

# BUILD

docker build -t docker-rest-api:1.0.0 .

# RUN

docker run -p 3000:3000 docker-rest-api:1.0.0
docker run --name v1-rest-api -d -p 3000:3000 docker-rest-api:1.0.0

# LOGS

docker logs -f v1-rest-api

# ACCESS SH

docker exec -it v1-rest-api

# PUSH TO DOCKERHUB

docker tag local-image:tagname new-repo:tagname
docker push new-repo:tagname

# PULL FROM DOCKERHUB

docker run --name v2-rest-api -d -p 3000:3000 nguyenbinh98/docker-rest-api:1.0.0
