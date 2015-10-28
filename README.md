# README #

This is an Ansible playbook that configures a fresh install of Debian 7.x for devops use. See roles for a list of services it installs.

To bootstrap a completely new installation: `ansible-playbook -i inventory playbooks/all.yml --ask-sudo-pass --ask-pass`

Ansible will prompt for 3 passwords: 1) root password, 2) sudo password, and 3) dev user password. 2 and 3 should be the same. 

After playbooks/setup runs, it will not run successfully again because it disables root access to the server.
