# stack-rackspace-marathon
Ansible script to deploy Marathon on Rackspace


pip install ansible
pip install pyrax
pip install --upgrade rackspace-novaclient
pip install os_virtual_interfacesv2_python_novaclient_ext


# Rackspace

# CoreOS bootstrap
Installed sigma.coreos-bootstrap from ansible-galaxy and moved it to roles to
keep it in the project.
Added roles in inventory.

# Deploy

```
ansible-playbook -v --private-key=~/.ssh/<private key> --user=root  --extra-vars "group=dev-mesos state=present" site.yml
```
