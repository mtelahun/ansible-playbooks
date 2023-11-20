VPS Common
=========

Configure's an Ubuntu machine with initial user, applications, and configurations

Requirements
------------

- community.general.ufw

Role Variables
--------------

- primary_user - The initial user to create. *Default: mtm*

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - vps_common
           vars:
             primary_user: "mtm"

License
-------

BSD-2-Clause

Author Information
------------------

Michael Telahun Makonnen <michael.telahun@dindin.et>
