docker-compose build

docker tag k3s-docker_server:latest pjabadesco/k3s-docker:0.3
docker push pjabadesco/k3s-docker:0.3

docker tag pjabadesco/k3s-docker:0.3 pjabadesco/k3s-docker:latest
docker push pjabadesco/k3s-docker:latest

docker tag pjabadesco/k3s-docker:latest ghcr.io/pjabadesco/k3s-docker:latest
docker push ghcr.io/pjabadesco/k3s-docker:latest
