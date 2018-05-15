network_snapshot Ansible Galaxy Role
=========

Role to take snapshot of all running-configurations of all network devices defined in ansible group. This role would
1) Configure requirements of OS for scp to work
2) Copy running-config to media on OS
3) Get config file to controller
4) Clean temporary files created on media of network OS

Configurations would be stored locally on ansible controller with naming convention as ansible-{{ ansible_host }}-{{ timestamp }}.cfg

This role extends the config backup options available on individual network element to all network elements
present in inventory group.


Requirements
------------
- scp python package should be installed 

Role Variables
--------------

Dependencies
------------
- network_get module (r2.6).

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
