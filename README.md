# ansible-solaris

Ansible configuration for OpenIndiana Hipster 2023.10 / OmniOS v11

Add pub ssh key to `/root/.ssh/authorized_keys` then run:

```
sed -ri 's/^(PermitRootLogin) .*/\1 prohibit-password/' /etc/ssh/sshd_config
svcadm enable ssh
svcadm restart ssh

# OpenIndiana only: This will ask for new root password on ssh login
rolemod -K type=normal root

pkg update
```

Check:
`ansible-playbook -v -C -i inventory main.yml`

Run with:
`ansible-playbook -v -i inventory main.yml`
