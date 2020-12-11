# nnnd_switch_security
nd_switch_security is a repository which will push secure configuration defined by **TGRC** on **Cisco IOS** switches using  **Ansible Playbooks** . 
**Secure configuration** refers to **security** measures that are implemented on network devices in order to reduce unnecessary cyber vulnerabilities.

## Host File

Inventory files are defined in separate repository # **[nd_host_files](https://git.cglcloud.com/NetworkInfrastructure/nd_host_files)** 

## Playbooks

This repository will have multiple playbooks, each contain a separate **TASK** . 
All tasks are getting imported in main playbook called **main.yml**.
Main playbook has potential to skip any task by adding **#** at the beginning of respective task.

[main.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/main.yml "main.yml") this is a matser playbook it will have all below sub-playboks

[aaa_config.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/aaa_config.yml "aaa_config.yml") this playbook will configure centralized management AAA commands.

[banner_motd.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/banner_motd.yml "banner_motd.yml") this playbook will configure legal notification banner upon all terminal.

[global_config.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/global_config.yml "global_config.yml") this playbook will Restrict available terminal and management ports and services.

[hostname.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/hostname.yml "hostname.yml") this playbook will conifigure **hostname** on switch.

[line_vty.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/line_vty.yml "line_vty.yml") this playbook will disable all terminal ports that are not explicitly required or actively being used.

[ntp_server.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/ntp_server.yml "ntp_server.yml") this playbook will Configure NTP across all devices.

[remove_ftp_tftp.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/remove_ftp_tftp.yml "remove_ftp_tftp.yml") this playbook will remove any configuration related to FTP or TFFT services.

[remove_nonstanderd_username.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/remove_nonstanderd_username.yml "remove_nonstanderd_username.yml") this playbook will delete any non-standard unsername.

[security_acl.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/security_acl.yml "security_acl.yml") this playbook will configure ACL's related to SNMP.

[snmp_config.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/snmp_config.yml "snmp_config.yml") this playbook will conifgure SNMP traps.

[syslog_siem_config.yml](https://git.cglcloud.com/NetworkInfrastructure/nd_switch_security/blob/test/syslog_siem_config.yml "syslog_siem_config.yml") this playbook will configure syslog server.

## Running the playbok

Use the `ansible-playbook` command:
```
ansible-playbook -i nd_switch_security_lab main.yml
```

## Additional Files

**group_vars** - this is a directory that contains variables separated by group  It is recommended to have a group per network platform type to store platform specific variables.

**group_files** this is a directory that contains config or text files those are being called under playbook.

The nd_switch_security is a repo which will show how to push secure configuration defined by **TGRC** on cisco ios switch with the help of  **Ansible Playbooks**.

## Mantainer

Currently, the CNetOps teams is the mantainer of this playbook.

# Code Owners

The CODEOWNERS file defines who has the ultimate authority to merge to protected branches.
As per the Product Owner's request, the sole code owner of the nd_switch_security repository is 
The Network Infrastructure Organization has two Owners:
* AnsiblePSAutomationAccount3
These two owners have full administrative access to all the repos within the organization and therefore, can also merge code.
 is the lead automation engineer and the owner of the organization.
AnsiblePSAutomationAccount3 is our process ID that the network automation team uses for automated proccess and therefore, owner level access is required.