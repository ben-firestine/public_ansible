This playbook checks a managed machine in order to make sure it is compliant with our gidelines. Currently, the playbook will check for the following compliance issues:

1. Has the computer been updated in the last 90 days?
2. Are the approved firewall rules still in place?
3. Are there any un-approved local users on this machine?

Variables that are used in this playbook:

===global variables===

- reachable: This contains all the hosts that are currently online and reachable by Ansible

- date: This gets the current date, mainly used for file creation as well as for checking when the computer was last updated

- excel_loc: This stores the location of the compliance excel document

- issue_count: This counts the amount of issues discovered in total so that it can be complied in an email

===system_update variables===

- system_status_result: This stores whether there is an issue with the computer or not. Defaults to an issue in case something in the playbook breaks

- compliance_date: This stores the date 90 days in the past to compare with

- last_update: This stores the date of when the remote machine was last updated

===local_user_check variables===

- local_users: This stores a list of all local users on the remote machine

- non_approved_users: This stores any users that are local and not on the list of approved users

- approved_users: This contains an array of pre-approved local users. Mostly consists of system users.

===firewall_check variables===

- remote_firewall_rules: This stores the remote machines firewalld rules

- approved_firewall_rules: This stores the list of approved firewall rules we have in place

- firewall_results: This stores the results of the compliance check. Defaults to a negative just in case there is an issue with the playbook
