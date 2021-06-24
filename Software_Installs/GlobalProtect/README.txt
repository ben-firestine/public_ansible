This playbook installs the GlobalProtect VPN onto Ubuntu based machines. There is currently no support for Redhat but that is planned for the future

Variables used in this playbook:

===global variables===

- reachable: This variables is used for getting a list of hosts that are online and reachable via SSH

- path: This is the install path of GlobalProtect. This is mainly used for verify that the application had be installed correctly

- application: This stores the name of the current application getting installed. This is used when sending emails to the customer

- ssh_port: This variable is used for if the server has a custom SSH port
