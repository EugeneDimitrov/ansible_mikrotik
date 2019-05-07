# Mikrotik Ansible Playbooks
## routeros_gen_upd_device_list.yml

This playbook generates list of Mikrotik devices which requires OS update. It uses routeros_command module to collect output from devices, a jinja2 template to generate device list file.
- **group_vars/routeros-devices**      
Variable "routeros_branch" represents required OS version branch, e.g. development, long-term, stable or testing.
- **hosts** 
Simple inventory file.
- **output/routeros_device_update.txt**  
Generated file with device list, e.g.       
    ```
    Mikrotik OS version info:
      Hostname: chr-1
      Installed-version: 6.43.14
      Latest-version: 6.44.3
      WARNING!!!: "This OS version is not from long-term branch, it is stable"
    ```
