Role Name
=========

Install the ArgoCD Operator (non-OLM).

Role Variables
--------------
`scope` defaults to namespace. Valid values are namespace or cluster.

`state` defaults to `present`. Valid values are present or absent.

`kubeconfig` defaults to `$HOME/.minishift/machines/minishift_kubeconfig`

`namespace` defaults to argocd.


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
