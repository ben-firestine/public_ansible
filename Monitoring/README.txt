This playbook is used for monitor certain aspects of a remote machine. This is to allow Administrators and owners of servers to better monitor for issues that might rise up on their machine. 

Variables that are used in this playbook:

===global variables===

- default_list: This is the default mail list for ALL playbooks

- main_list: This is initially un-defined as it needs to be blank. This is used for combining the default and custom mail lists together

- custom_list: This is a custom mail list that is attached to the specific inventory file.

- ssh_port: Default value is 22. You may add a inventory variable to change the value of this variable. This would be useful if you had a custom SSH connection port

- alert: This is used for monitoring if there is an alert that needs to be sent out via email

- monitor: The syntax for this command is as follows. "<num>,<num2>". If you only have one monitor to check, just put in that number. This indicates what playbooks the inventory wants run on hosts. This variable MUST be defined in the inventory file. 
    - 1: This is the playbook for checking the raid status of a machine
    - 2: This is the playbook for checking the storage availability of a machine
    - 3: This is the playbook for checking the CPU and RAM stats of a machine

- Threshold: Default value is 80%. This is used for determining what triggers an ALERT. This can be changed with a variable in the inventory file

===storage variables===

- default_storage: Default value is /. This is the default directory that gets checked by the playbook. This will get checked along with any custom storage locations

- custom_storage: This is the custom storage locations that are defined as a variable in the inventory file

- main_storage: This is initially un-defined as it needs to be blank. This is used for combining the default and custom storage variables

- storage_output: This stores the output of the TOP command

- storage_status: Default value is GOOD. This will indicate if there are any problems with the storage devices checked

===RAID variables===

- zpool_status: This stores the results of the ZFS command

===System Usage variables===

- system_cpu: Default value is 0. This stores the average load of the system

- user_cpu: Default value is 0. This stores the average load of the user

- mem_total: Default value is 0. This stores the total memory available to the system

- mem_used: Default value is 0. This stores the amount of memory that is currently being used by the system

- percent_used: Default value is 0. This stores the precent of RAM that is being used by the system
