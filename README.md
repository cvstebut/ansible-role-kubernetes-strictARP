Role Name
=========

This Ansible role sets the strictARP setting in the kube-system/kube-proxy namespace.

The processing is done on the controller node by way of the k8s* modules.

Requirements
------------

### Install Ansible collection `community.kubernetes` on Ansible controller

```console
ansible-galaxy collection install community.kubernetes
```

### Install openshift python module

```console
pip3 install openshift
```

Role Variables
--------------

```yaml
---
# vars file for ansible-role-kubernetes-strictarp
kubernetes_strictARP: true
kubernetes_kubeconfig: /home/ansible/.ci/kubeconfig/kubeconfig_minikube04/config
kubernetes_context: "minikube04"
```

- `kubernetes_strictARP: [true|false]`
- `kubernetes_kubeconfig`: Valid kubeconfig file for accessing the desired context
- `kubernetes_context`: Targetes Kubernetes context (cluster)

Dependencies
------------

See requirements

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
---
- hosts: localhost
  roles:
    - ansible-role-kubernetes-strictarp
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
