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

### Vault variables
- vault_kopia_b2_bucket
- vault_kopia_b2_password
- vault_kopia_b2_application_id
- vault_kopia_b2_access_key
- vault_kopia_repository_token

### Regular variables
- install_ui - default:false
- kopia_user - default: "root"
- kopia_group - default: "root"
- kopia_config_user - default: "{{ kopia_user}}"
- kopia_config_group - default:  "{{ kopia_group }}"
- kopia_config_path - default: "/{{ kopia_user }}/.config/kopia"
- kopia_cache_root - default: /{{ kopia_user }}/.cache
- kopia_backup_sources - default: /home/mtm
- kopia_backup_retention_hourly - default: 6
- kopia_backup_retention_daily - default:  7
- kopia_backup_retention_weekly - default:  5
- kopia_backup_retention_monthly - default: 12
- kopia_backup_retention_annual - default: 1

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
