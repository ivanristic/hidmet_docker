# hidmet_docker

cd hidmet_docker

docker-compose -f docker-compose-registry.yml up -d
docker-compose -f docker-compose-liberty-server.yml build
docker-compose -f docker-compose-hidmet.yml build

docker stack deploy -c docker-stack.yml hidmetstack
