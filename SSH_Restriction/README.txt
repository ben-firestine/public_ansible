This playbook is used for locking down SSH based connections to approved IP addresses/ranges. 

The current list of approved IP addresses/ranges:

- Example whitelist
  
  source: X.X.X.X/24

===global variables===

- reachable: This variable is used to store a list of all the hosts that are online and reachable via SSH

- ssh_port: This is for custom SSH ports. Default value is 22
