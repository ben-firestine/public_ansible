This playbook updates a remote machine with the latest packages that are available. It will also remove any dependencies that are no longer needed.

Variables that are used in this playbook:

===global variables===

- package_simulate: This variables contains a list of packages that need an update. This variable is used when I send out an email to the customer with what was updated

- update: This boolean variable is used for checking to see if there was any packages updated

- check_reboot: This checks to see if the remote machine needs to reboot after updating packages

- restart_msg: This stores a string message that is used when sending an email to the customer

- hour: This stores the hour variable for when the remote machine needs to be restarted

- minute: This stores the minute variable for when the remote machine needs to be restarted

- second: This stores the second variable for when the remote machine needs to be restarted

- time: This combines the above three variables into one time that is then sent to the customer via email

- ssh_port: This variable allows for custom SSH ports on specific servers
