## docker-swarm

```
$ docker swarm init && docker network create --driver=overlay traefik-public

$ git clone https://github.com/wuhanstudio/authelia-docker-swarm

$ cd authelia-docker-swarm

# Replace with your own domain
$ find . -type f -name "*.yml" -exec sed -i'' -e 's/example.com/wuhanstudio.cc/g' {} +

$ docker stack deploy -c traefik-compose.yml traefik
```
