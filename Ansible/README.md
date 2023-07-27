# Ansible

This development environment sets up Ansible in a docker container. Using the commands below, you can run your playbook in the docker container without the need of installing ansible and any dependencies on your host machine.

Build the container:
```
docker build -t ansible .
```

Run your playbook in the container:
```
docker run -t --rm -v ./ansible:/src -w /src vcenter_ansible ansible-playbook playbook.yml
```
_Note: make sure to verify that the paths provided are accurate_
