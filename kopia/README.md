Kopia
=========

Install, configure and run Kopia backup to a remote B2 repository.

Requirements
------------

Ensure that you have already created and initialized the remote repository with: 
```
kopia repository create b2 --bucket=... --key-id=... --key=...
```
Then run `kopia repository status -st`. This will print a bunch of information about your repository. Copy the value of the repository token to a variable
in your vault called `vault_kopia_repository_token`.


Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: kopia }

License
-------

BSD-2-Clause

Author Information
------------------

Michael Telahun Makonnen <michael.telahun@dindin.et>
