docker-compose build

docker tag docker-k3s_server:latest pjabadesco/docker-k3s:0.6
docker push pjabadesco/docker-k3s:0.6

docker tag pjabadesco/docker-k3s:0.6 pjabadesco/docker-k3s:latest
docker push pjabadesco/docker-k3s:latest

docker tag pjabadesco/docker-k3s:latest ghcr.io/pjabadesco/docker-k3s:latest
docker push ghcr.io/pjabadesco/docker-k3s:latest
