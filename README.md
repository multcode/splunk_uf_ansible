# Splunk Cloud Universal Forwarder Builder

_Example Ansible Playbooks for Rapidly Building Splunk Universal Forwarders_

## Overview

These Ansible playbooks are designed to build Splunk Universal Forwarders to work in conjuction with a Splunk Cloud deployment.

## Customization Details

Scripts use a "static_files" directory in the remote user's home directory on the target system for staging and comparing files. Replace "/home/remoteuser" with the path to the home directory of the remote user on your target systems.

Change splunk admin password in group_vars/all and encrypt with ansible-vault

Place the Splunk Forwarder DEB file in roles/splunk_forwarder_uf/files
Add the filename of the Splunk Forwarder DEB to the task file roles/splunk_forwarder_uf/files/install_uf.yml

Replace the inputs.conf file in roles/splunk_forwarder_uf/files with your own

Add your credentials file splunkclouduf.spl to roles/splunk_forwarder_uf/files 

Change the admin user password in roles/splunk_forwarder_uf/files/user-seed.conf with your own, then encrypt with ansible-vault

