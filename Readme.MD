minikube start
minikube tunnel 941230

docker pull willhallonline/ansible:2.16-ubuntu-22.04
docker run --rm --name=zabbix-proxy willhallonline/ansible:2.16-ubuntu-22.04 /bin/sh -c "while true; do sleep 1000; done"
ANSIBLE_ALLOW_BROKEN_CONDITIONALS=true