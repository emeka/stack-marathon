# stack-rackspace-marathon (This is WIP)
Ansible script to deploy Marathon on Rackspace using CoreOS.

# Dependencies

You will need Python 2.7.x and pip

pip install ansible
pip install pyrax
pip install --upgrade rackspace-novaclient
pip install os_virtual_interfacesv2_python_novaclient_ext --upgrade


# Rackspace

# CoreOS bootstrap
Installed sigma.coreos-bootstrap from ansible-galaxy and moved it to roles to
keep it in the project.

# Deploy

Use the following command to deploy a dev environment:

```
ansible-playbook -v --private-key=~/.ssh/<private key> --extra-vars "env=dev state=present key_name=<ssh key name>" site.yml
```

Use the following command to remove the dev environment:

```
ansible-playbook -v --private-key=~/.ssh/<private key> --extra-vars "env=dev state=absent key_name=<ssh key name>" site.yml
```


