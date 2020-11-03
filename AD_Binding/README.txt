This playbook takes a computer or VM that is not bound to Active Directory and installs, configures and binds it to Active Directory. It does this with the realmd and sssd packages
along with configuration files that are provided by us. 

Variables that are used in this playbook:

===global variables===

- vault_user: This stores the user of an administrator for use when binding to AD

- vault_password: This stores the password for the above user

- reachable: This variable is used to store a list of all the hosts that are online and reachable via SSH

===initial_config variables===

- hostname: This would be the what the IT administrator wants the hostname of the computer to be

===bind variables===

- AD_DOMAIN: This stores the Active Directory OU information

- bind_domain: This stores the AD object location

===ssh_sudo_access variables===

- ssh_group: This is the name fo the SSH security group

- sudo_group: This is the name of the sudoers security group

- ansible_group: This is the name of the special Ansible group that is added to all new computers
