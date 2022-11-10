# role-crowdsec
The open source &amp; collaborative security IPS 


## Initial setup

### Example playbook
```
- hosts: crowdsec_agent
  become: yes

  vars:
    # -- roles/role-crowdsec --
    crowdsec_console_enroll_key: '{{ def_crowdsec_enroll_key }}'

  roles:
    - role-crowdsec

  tasks:
```

## Running after applying role
- Login on ``app.crowdsec.net`` and accept enrollment;
- Restart service on host ``systemctl restart crowdsec`` or reboot the host;

