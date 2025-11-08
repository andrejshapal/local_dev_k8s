source /home/andrejs/.virtualenvs/MDM/bin/activate
minikube start
minikube tunnel 941230
ansible-playbook -i inventory/all.yaml proxy.yaml
 ansible-playbook -i inventory/all.yaml kubernetes.yaml --vault-password-file ~/secrets.pass
docker pull willhallonline/ansible:2.16-ubuntu-22.04
docker run --rm --name=zabbix-proxy willhallonline/ansible:2.16-ubuntu-22.04 /bin/sh -c "while true; do sleep 1000; done"
export ANSIBLE_ALLOW_BROKEN_CONDITIONALS=true