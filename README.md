gitmcredinit 
===============

Initialize global credentials (user.name and user.email) for multiple users on development a machine

Requirements
----------------

Git must be installed on the target system. Requires root user.

Role Variables
-----------------

| Variable | Description    |
| -------- | -------------- |
| users    | Array of users |

### User Item description ###

| Variable | Description         |
| -------- | ------------------- |
| user     | System user account |
| name     | Full name of user   |
| email    | Email               |

Dependencies
------------

No role dependencies

Example Playbook
----------------

    - name: Init git on host
      hosts: dev_machine
      vars:
         users:
             - 
              user: "robert"
              name: "Robert Example"
              email: "robert@example.com"
             - 
              user: "anna"
              name: "Anna Example"
              email: "anna@example.com"
          
      roles:
        - cyborg_x1.gitmcredinit

License
-------

BSD

Author Information
------------------

Christian Holl:  cyborgx1 [the at] gmail [the dot] com
