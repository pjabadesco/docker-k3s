docker-compose build

docker buildx build --platform=linux/amd64 --tag=docker-k3s_server:latest --load .

docker tag docker-k3s_server:latest pjabadesco/docker-k3s:0.10
docker push pjabadesco/docker-k3s:0.10

docker tag pjabadesco/docker-k3s:0.10 pjabadesco/docker-k3s:latest
docker push pjabadesco/docker-k3s:latest

docker tag pjabadesco/docker-k3s:latest ghcr.io/pjabadesco/docker-k3s:latest
docker push ghcr.io/pjabadesco/docker-k3s:latest
