gitmcredinit 
=========

Initialize global credentials (user.name and user.email) for multiple users on development a machine

Requirements
------------

Git must be installed on the target system. Requires root user.

Role Variables
--------------

     users: #array of users for a machine
         - 
          user: "robert" #username on the machine
          name: "Robert Example" #git config --global user.name 
          email: "robert@example.com" #git config --global user.email
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
        - role: gitmcredinit

License
-------

BSD

Author Information
------------------

Christian Holl:  cyborgx1 [the at] gmail [the dot] com
