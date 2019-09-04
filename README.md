# LOCAL VM with Docker
Those playbooks configure a VM (f.e. libvirt-based) as a docker host,
providing similar expirience to docker-machine (which is Win/Mac only).

It also updates home .bashrc for user to set `DOCKER_HOST` to a proper value.

Prerequirements:

* configured and operational ubuntu/debian VM with passwordless sudo.
* your own inventory (see `inventory.yaml`) for guidance.

##How to run

```
ansible-playbook -i your_inventory.yaml vm.yaml
ansible-playbook -i your_inventory.yaml docker.yaml
```

You need to open a new shell (new terminal)
to have your updated `.bashrc` been applied.
