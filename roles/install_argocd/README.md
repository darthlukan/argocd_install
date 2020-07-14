Role Name
=========

Install the ArgoCD Operator (non-OLM).

Role Variables
--------------

`state` defaults to `present`.

`kubeconfig` defaults to `$HOME/.minishift/machines/minishift_kubeconfig`


Example Playbook
----------------
```
- name: Install ArgoCD Operator
  hosts: local
  tasks:
    - import_role:
        name: install_argocd
```
License
-------

Apache-2.0, see LICENSE file in parent collection
