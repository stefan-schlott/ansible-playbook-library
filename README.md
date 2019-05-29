The following selection of ansible scripts assume that you are operating on an environment that was successfully setup with dcos-ansible ( https://github.com/dcos/dcos-ansible )  and that you can use its Ansible inventory.

All the examples given here assume that the Ansible playbook execution is run from the base folder of dcos-ansible (and its inventory).

Furthermore most of the higher-level scripts assume that the Bootstrap node of the DC/OS cluster has to dcos cli installed and configured to execute commands against the DC/OS cluster.

To set that up, you initially need to run the following things


```
cd <base folder of dcos-ansible>
ansible-playbook <local checkout path of this repository>/dcos/general/install-dcos-cli-on-boostrap-node.yaml
``` 
