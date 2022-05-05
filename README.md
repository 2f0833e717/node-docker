<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [写経リポジトリ](#%E5%86%99%E7%B5%8C%E3%83%AA%E3%83%9D%E3%82%B8%E3%83%88%E3%83%AA)
- [command](#command)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 写経リポジトリ
元ネタ

[Youtube] [Google自動翻訳]

Dockerを学ぶ-Node.jsとExpressを使用したDevOps

https://www.youtube.com/watch?v=9zUHg7xjIqQ

# command

```docker
sudo service docker stop
sudo service docker start

docker build .
docker image ls
docker run -d --name node-app node-app-image
docker ps
docker ps -a
docker rm -f node-app
docker run -p 3000:3000 -d --name node-app node-app-image
docker exec -it node-app bash
docker run -v $(pwd):/app -p 3000:3000 -d --name node-app node-app-image
#[windows]docker run -v %cd%:/app -p 3000:3000 -d --name node-app node-app-image
docker logs node-app
docker run -v $(pwd):/app -v /app/node_modules -p 3000:3000 -d --name node-app node-app-image
docker run -v $(pwd):/app:ro -v /app/node_modules --env PORT=4000 -p 3000:4000 -d --name node-app node-app-image
docker run -v $(pwd):/app:ro -v /app/node_modules --env-file ./.env -p 3000:4000 -d --name node-app node-app-image
docker volume ls
docker volume prune

docker compose up -d
docker compose down -v
docker compose up -d --build
docker compose -f docker-compose.yml -f docker-compose.dev.yml up -d
docker compose -f docker-compose.yml -f docker-compose.dev.yml down -v
docker exec -it node-docker-mongo-1 bash
docker exec -it node-docker-mongo-1 mongo -u "admin" -p "admin"
docker inspect node-docker-mongo-1
docker network ls
docker logs node-docker-node-app-1 -f
docker network node-docker-node-app-1
docker compose -f docker-compose.yml -f docker-compose.dev.yml up -d --no-deps node-app
docker compose -f docker-compose.yml -f docker-compose.dev.yml up -d mongo
docker compose -f docker-compose.yml -f docker-compose.dev.yml up -d node-app
docker compose -f docker-compose.yml -f docker-compose.prod.yml up -d
docker compose -f docker-compose.yml -f docker-compose.prod.yml down 
docker compose -f docker-compose.yml -f docker-compose.dev.yml restart
docker logs node-docker-mongo-1 -f | jq
```
