Network_snapshot Ansible Galaxy Role
=========

Role to take a snapshot of all devices running-configurations defined in ansible group. Configurations would be
stored locally on ansible controller with naming convention as ansible-{{ ansible_host }}-{{ timestamp }}.cfg

Config backup options as available on individual network element can be extended to all network devices using this
module.

Requirements
------------
- scp

Role Variables
--------------

Dependencies
------------
- network_get module eleased in Ansible 2.6.

Example Playbook
----------------

  - name: run the role
    hosts: all

    roles:
      - network_snapshot

License
-------

BSD

Author Information
------------------

ansible-network-team
