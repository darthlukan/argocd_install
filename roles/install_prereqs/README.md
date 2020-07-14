install_prereqs
=========

A role to install prerequisites for using ArgoCD (arcocd, kubectl, oc cli tools).

Role Variables
--------------

`bin_dir` defaults to `$HOME/bin`

`ocp_major_version` defaults to `4`


Example Playbook
----------------

```
- name: Install Prerequisites
  hosts: local
  tasks:
    - import_role:
        name: install_prereqs
```

License
-------

Apache-2.0, see LICENSE file in parent collection
