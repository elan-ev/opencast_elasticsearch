Ansible: Opencast Elasticsearch Role
====================================

This Ansible role installs and prepares Elasticsearch for Opencast.
This role expects Elasticsearch to be installed on Opencast's admin node.

Role Variables
--------------

- `opencast_repository_identifiers`
  - List of repository identifiers to temporarily activate for integration
  - Will usually be provided by the [elan.opencast_repository](https://github.com/elan-ev/opencast_repository) role
- `opencast_elasticsearch_heap_size`
  - Memory configuration (default: `1g`)
  - Might make sense to set this to `2g` for larger installations.

Dependencies
------------

This role requires `elan.opencast_repository`.


Example Playbook
----------------

Example of how to configure and use the role:

```yaml
- hosts: servers
  become: true
  roles:
    - role: elan.opencast_elasticsearch
```
