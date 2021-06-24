This playbook will take a computer or Virtual Machine that is not bound to Active Directory and install, configure, and bind it. This is accomplished with the realmd and sssd packages along with pre-configured files provided by the IT administrators.


===global variables===

- vault_user: This variable stores the username of the Administrator for Active Directory. This is vaulted so that the credentials are protected.

- vault__password: This variable stores the password for the above Administrator. This is vaulted so that the credentials are protected. 

- default_list: This is the default mail list for ALL playbooks

- main_list: This is initially un-defined as it needs to be blank. This is used for combining the default and custom mail lists together

- custom_list: This is a custom mail list that is attached to the specific inventory file.

- ssh_port: Default value is 22. You may add a inventory variable to change the value of this variable. This would be useful if you had a custom SSH connection port

===initial_config variables===

- hostname: This is used to set the hostname of the computer. AWX asks the Administrator to input a value for this variable on run

===bind variables===

- AD_DOMAIN: This stores the root Active Directory OU and is used as a placeholder throughout the playbook

- bind_domain: This variable points to the OU location that you want the computer object to go to

- local_pass: This variable will contain an encrypted, secure password for the computers local account

- ad_hostname: The default value is: "{{ hostname }}.tld.domain.com". This contains the FQDN hostname of the machine. This will be used to setup DDNS.

===ssh_sudo_access variables===

- ssh_group: This is used for giving SSH permission to an AD group

- sudo_group: This is used for giving SUDO permission to an AD group

- ansible_group: This is used for giving SUDO access to the Ansible server
