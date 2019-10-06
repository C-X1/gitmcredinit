ansible-gitmcredinit 
=========

Initialize global credentials (user.name and user.email) for multiple users on development a machine

Requirements
------------

Git must be installed on the target system. Requires root user.

Role Variables
--------------

     users:
         - 
          user: "robert"
          name: "Robert Example"
          email: "robert@example.com"
         - 
          user: "anna"
          name: "Anna Example"
          email: "anna@example.com"

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
        - role: ansible-gitmcredinit

License
-------

BSD

Author Information
------------------

Christian Holl:  cyborgx1 [the at] gmail [the dot] com
