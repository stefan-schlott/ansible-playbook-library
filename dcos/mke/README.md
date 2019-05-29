# install MKE
https://docs.mesosphere.com/services/kubernetes/ 

To install DC/OS MKE (Multi Kubernetes) do the following thing:

```
cd <base folder of dcos-ansible>
ansible-playbook <local checkout path of this repository>/dcos/mke/install-mke.yaml
``` 

# install two Kubernetes clusters using MKE on the configured cluster
After MKE is successfully installed and running, you can install two Kubernetes clusters the following way:


```
cd <base folder of dcos-ansible>
ansible-playbook <local checkout path of this repository>/dcos/mke/install-kubernetes-cluster.yaml -e @~/GIT-repos/github/stefan-schlott/ansible-playbook-library/dcos/mke/vars/extra-vars-kube1-dcos.yml
``` 

```
cd <base folder of dcos-ansible>
ansible-playbook <local checkout path of this repository>/dcos/mke/install-kubernetes-cluster.yaml -e @~/GIT-repos/github/stefan-schlott/ansible-playbook-library/dcos/mke/vars/extra-vars-kube2-dcos.yml
``` 