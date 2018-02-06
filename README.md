# ansible-eos
This repository contains a set of ansible playbooks, roles, templates and variable files used to configure interfaces, as well as bgp underlay and overlay configurations sufficient to configure an eight node (2 Spine, 6 leaf) environment.

The site.yml playbook calls the leaf.yml and spine.yml plays, which in turn assigns a role based on a host's group (leaf or spine) id in the /etc/ansible/hosts file.  The Roles then call on thier respective tasks, which merg the information in the template file with the information contained in host_vars. 
