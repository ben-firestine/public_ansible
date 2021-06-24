===Overview===

This playbook tasks a directory provided by the user and backs it up to another location provided by the user. This is usually some sort of network share drive so that the data is secured offsite.

===Global Variables===

date: This contains the current date at the time of run

loc_output: This variable stores the log output when the backup is run

default_list: This contains the default mail list for Ansible

ssh_port: Default value is 22. This stores the port that ssh tries to connect on. This is useful for if you have a custom ssh port

main_list: This is the main email list that Ansible sends email to


