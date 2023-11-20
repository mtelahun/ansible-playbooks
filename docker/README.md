Docker
=========

Install docker-ce

Requirements
------------

None

Role Variables
--------------

- ubuntu_codename - Ubuntu release code name (default: jammy)

Dependencies
------------

- vps_common

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - vps_common
         - docker
            vars:
              ubuntu_codename: "jammy"

License
-------

BSD-2-Clause

Author Information
------------------

Michael Telahun Makonnen <michael.telahun@dindin.et>
