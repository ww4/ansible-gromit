# Notes on getting server setup

Following this guide: https://opensource.com/article/18/3/manage-workstation-ansible

using ansible-pull to avoid needing server (for now)

add ansible repository
install ansible
install git
sudo ansible-pull -U https://github.com/ww4/ansible-gromit.git
Failed to install apt packages, "no package matching google-chrome-stable"
Need to update git repo - need passwords - need to install Bitwarden
added Bitwarden extension to Firefox
added SSH key to Git
cloned Git repo for tuning Ansible
installed VSCode
using VSCode to work on Git - wonderful integrations!
installed gnome-tweaks to get capslock remap to super
installed xbindkeys, not sure if needed
installed ansible on Bub - I want to go all-in learning Ansible
created hosts file on Bub /etc/ansible/hosts
Start over - now following Geerling's book. 
Install Vagrant on bub
spun up centos7 with vagrant, typed out playbook from book
two "end" statements at end of vagrantfile
destroyed centos7, downloaded vagrant box for ubuntu22.04 (same as gromit)
Playbook failed, tweaked 'yum' to generic "package", worked
skipping chapter ad-hoc commands
Time to venture out... first draft

Playbook notes:
 - add repositories first
 - write a dependency tree
 - core services like Docker installed first
 - group services by type - GUI tweaks, server apps, desktop apps
 - Split out packages as individual tasks to prevent one failure aborting others
 
 
 How quick can I get a system ready for Ansible provisioning?
  - install system from livedisk
  - install Tailscale
  - install Ansible
  - add tailscale IP to ansible hosts
  - run ansible


Loaded Git repo into work VSCode editor
Split packages list into smaller bites
cloned github ansible-gromit repo onto Bub
updated Vagrantfile to use repo, test run, "no hosts matched"
managed to run ansible against gromit using -K for passwd and -i specify hosts file


This looks useful. https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-docker-on-ubuntu-20-04

following above tutorial, added docker.yml to tasks
