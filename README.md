# Ansible Collection - darthlukan.argocd_install

Author: Brian Tomlinson <btomlins@redhat.com> / <darthlukan@gmail.com>


## Description

`argocd_install` is an Ansible Collection that provides two roles, `install_prereqs` and `install_argocd` which install
the prerequisites for working with ArgoCD on Kubernetes and OpenShift and installs the ArgoCD Operator (non-OLM)
respectively.


## Installation

```
$ ansible-galaxy collection install darthlukan.argocd_install
```


## Usage

```yaml
---
- name: Install ArgoCD Operator and cluster tools
  hosts: local
  tasks:
    - import_role:
        name: darthlukan.argocd_install.install_prereqs
    - import_role:
        name: darthlukan.argocd_install.install_argocd
...
```


## License

Apache-2.0, see LICENSE file.
