# Purpose

This repository contains testing playbooks and examples when using Ansible 2.4.2 modules.

- net_provision.yml - Playbook example of using the net_ modules http://docs.ansible.com/ansible/latest/net_vlan_module.html
- role_provision.yml - Pushing all logic into roles and using a OS agnostic approach but using the OS specific modules eos_, nxos_, ios_
- eos_provision.yml - Using the eos_ modules
- provision.yml - Pulling together all methods
- hosts - host files using ansible_network_os for the net_ modules

# Host_vars Breakdown

In this scenario, we are using an intended style of variable for each module to reduce business logic needed in templates and playbooks

The variables are setup for the corresponding module need for example:

net_interfaces: accepts interfaces for the aggregate as a 'list', interfaces is setup as a list in the variables

Other variables, no module was encountered that had specific type for variables for example:

- banner
- spanning_tree
- mlag
