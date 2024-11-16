A simple role to install Lemur on Debian.

This role requires the community.mysql collection. Unfortunately, Ansible will
not allow a [role to depend on a
collection](https://github.com/ansible/ansible/issues/76030#issuecomment-942520399),
which means you will need to manually install this collection before trying to
run this role. The collection can be installed with:

```
ansible-galaxy collection install community.mysql
```

# Examples
## Playbook
Here's an example of a playbook to install Lemur on the local machine. It does
not require you have SSH running.

```yaml
- hosts: localhost
  connection: local
  become: true
  roles:
    - role: hax0rbana_adam.lemur
```

To maek a playbook to run this role on a remote host:

```yaml
- hosts: all
  remote_user: root
  roles:
    - role: hax0rbana_adam.lemur
```

# Official repo location
All activity takes place on the official GitLab instance:
[https://gitlab.hax0rbana.org/public-repos/ansible/lemur](https://gitlab.hax0rbana.org/public-repos/ansible/lemur)

Any other hosting providers, such as GitHub.com and GitLab.com, are just mirrors
and we do not monitor the issue trackers over there.

# Support
## Matrix channel
You can also join our Matrix channel: #ansible:hax0rbana.org

This is a good place to ask questions or make requests without having to sign
up for another account.

# Contributing
See [contributor guidelines](CONTRIBUTING.md).

# License
This project is licensed under MIT License. See [LICENSE](LICENSE) for more details.
