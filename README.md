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

### Install the ArgoCD Operator as namespace scoped (default)

playbook.yaml:
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
CLI command:
```
$ ansible-playbook -i $INVENTORY playook.yaml
```

### Install the ArgoCD Operator as cluster scoped

playbook.yaml:
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
CLI command:
```
$ ansible-playbook -i $INVENTORY playbook.yaml -e scope=cluster
```

### Uninstall the ArgoCD Operator

playbook.yaml:
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
CLI command:
```
$ ansible-playbook -i $INVENTORY playbook.yaml -e stat=absent
```

*IMPORTANT!* If you do not want to remove the tools such as `kubectl`, `oc`, and `argocd` from the user's `~/bin`,
exclude the `darthlukan.argocd_instal.install_prereqs` role from your playbook!

## License

Apache-2.0, see LICENSE file.
