Network_snapshot Ansible Galaxy Role
=========

When something in a network goes catastrophically wrong, operators count on having a fall-back position: 
the ability to automatically go back to configure the last known good state. In SDN/VNF case, last good
state of network is always changing. This role takes snapshot of 'grouped'* network elements defined in 
ansible-inventory with following meta-data in a timeseries data-model

- running-configuration
- versions of main OS and active packages
- states - interfaces/protocol/user-defined states

This snapshot gives operator ability to 
1) Diffs of configuration or meta-data for last 'x' backups
2) Diffs of operations states for corresponding backups

'grouped' network elements are collection of network devices identified in fault group where a change
in one device configuration can affect others e.g peering edge routers, routers in an ospf area.
When a problem is detected in one of the elements then config can be rolled back to last good state
of the group. 

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
