# README #

This is an Ansible playbook that configures a fresh install of Ubuntu 14.x for devops use. See roles for a list of services it installs.

To bootstrap a completely new installation: `ansible-playbook -i [inventory file] playbooks/all.yml --ask-vault-pass --ask-sudo-pass --ask-pass`

Ansible will prompt for 4 passwords: 1) root password, 2) sudo password, 3) dev user password, and 4) vault pass. 2 and 3 should be the same. 4 is the password used for encrypted files.

After playbooks/setup runs, it will not run successfully again because it disables root access to the server.
