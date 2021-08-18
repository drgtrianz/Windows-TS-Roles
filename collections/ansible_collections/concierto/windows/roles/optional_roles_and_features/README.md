Role Name
=========

Use the role to install/uninstall Windows (optional) features.

Requirements
------------

Install/Uninstall Windows Features

Role Variables
--------------

[document reference](https://docs.ansible.com/ansible/latest/collections/ansible/windows/win_dsc_module.html) of Ansible.

```yml
# To install windows features
roles_and_features:
    'TelnetClients': true
# To uninstall windows features
roles_and_features:
    'TelnetClients': false
```
To list the windows features use the command 'Get-WindowsOptionalFeature' or 'Get-WindowsFeature' in powershell 

To capture the output in CSV capture_output role should be included while executing the playbook

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------


```yml
- hosts: all
  collections:
    - concierto.windows
  role:
    - optional_roles_and_features
```

License
-------

BSD

Author Information
------------------

Jayaganesh Kumar
