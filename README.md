## docker-swarm

```
$ docker swarm init && docker network create --driver=overlay traefik-public

$ git clone https://github.com/wuhanstudio/authelia-docker-swarm && cd authelia-docker-swarm

# Replace wuhanstudio.cc with your domain
$ find . -type f -name "*.yml" -exec sed -i'' -e 's/example.com/wuhanstudio.cc/g' {} +


# Replace wuhanstudio@qq.com with your email
$ find . -type f -name "*.yml" -exec sed -i'' -e 's/your@email.com/wuhanstudio@qq.com/g' {} +

$ docker stack deploy -c traefik-compose.yml traefik
```
