users
=====

This role adds/removes user accounts

Requirements
------------

None.

Role Variables
--------------

  user_accounts:
    - name: "John Doe"
      username: jdoe
      groups: group1
      shell: /bin/bash
      state: present
      key:
        active: 
          - id_rsa1
          - id_rsa2
        disabled: []

Dependencies
------------

None

Example Playbook
----------------

  - hosts: all
    roles:
      - { role: users,
          user_accounts:
            - name: "John Doe"
              username: jdoe 
        }

License
-------

MIT

Author Information
------------------

This role was created in 2018 by Keith Boyd-Carter Yale University Library IT
System Programmer
