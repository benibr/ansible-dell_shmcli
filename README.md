# DELL Server Hardware Manager CLI

This role installs the DELL Server Hardware Manager CLI.
The software is not available as a package but as a tar.gz containing a installer.

## Variables

* `dell_shmcli_download_link`: Download link from where the installer is downloaded. Defaults to the DELL Support Portal.
* `dell_shmcli_download_dir`: The directory where the installer is downloaded to. Defaults to `/tmp`.
* `dell_shmcli_state`: Whether SHM CLI should be present or absent. Defaults to `present`.

## Example playbook

```
- name: Install SHM CLI
  hosts: dell_servers
  roles:
    - dell_shmcli
```
```
- name: Remove SHM CLI
  hosts: dell_servers
  vars:
    dell_shmcli_state: absent
  roles:
    - dell_shmcli

```
