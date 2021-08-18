Role Name
=========

Use the role to Create/modifiy or remove Windows scheduled tasks.

Requirements
------------

Create/Modify/Remove the windows scheduled task 


Role Variables
--------------

[document reference](https://docs.ansible.com/ansible/latest/collections/community/windows/win_scheduled_task_module.html) of Ansible.

```yml
# Create/Modify the task scheduler
scheduled_tasks:
  - name: 'Notepad launcher'
    description: 'This task launch notepad evry Day at 12:00'
    actions:
      - path: 'c:\windows\system32\notepad.exe'
    triggers:
      - type: daily
        start_boundary: '2021-08-09T12:00:00'
    username: SYSTEM
    enabled: true
    state: present

# Remove the task scheduler
scheduled_tasks:
  - name: 'Notepad launcher'
    state: absent

```
To capture the output in CSV capture_output role should be included while executing the playbook

Example Playbook
----------------

```yml
- hosts: all
  collections:
    - concierto.windows
  role:
    - task_scheduler
```

License
-------

BSD

Author Information
--------------------
Jayaganesh Kumar