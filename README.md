ansible-dev-machine
===================
This is an Ansible playbook that aims to configure a newly Ubuntu installation with development tools.

Ansible installation
====================

	$ sudo add-apt-repository ppa:rquillo/ansible
	$ sudo apt-get update
	$ sudo apt-get install ansible

Starting orchestration
======================

	$ ansible-playbook dev-machine.yml -i inventory.yml --connection=local -K

If you want to select only some developer tools, you can select them with this command:

	$ ansible-playbook dev-machine.yml -i inventory.yml --connection=local -K --tags "`<some packages>`"

These are the available packages:

* system
* development
* browser
* ide
