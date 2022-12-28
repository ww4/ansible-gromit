### Plex Media Server playbook:

#### Vault & Bitwarden:

Sudo credentials are stored in Bitwarden, therefore you 
must have Bitwarden running for this to work.
ansible.cfg looks for the password in .vault_pass. This is not
a text file, it is a script which calls Bitwarden to search for the 
credentials. Bitwarden is configured to ask for the master password 
on runtime, pass the results to Ansible, then Ansible will run.

To avoid retyping the password every time, unlock Bitwarden by setting
the environment variable before running ansible.

#### Provisioning:

To set up the server, run the provisioning script:

   ansible-playbook provision.yml

(more to come, this project is a WIP)
