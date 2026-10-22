# cendio.thinlinc

Perform common best-practice tasks when configuring ThinLinc servers.

## Description

Besides installing [ThinLinc](https://cendio.com), there are a number of things which generally need to be done in order to get a fully functional ThinLinc system. For example:

 - ensuring ThinLinc's administration commands work with `sudo`
 - installing supported desktop environments
 - implementing distribution-specific [tweaks](https://cendio.com/thinlinc/docs/platforms)

This collection is designed to make administrators' lives easier when managing ThinLinc systems using Ansible.

## Requirements

 - `ansible-core` >= 2.15
 - [`thinlinc-server`](https://github.com/cendio/ansible-role-thinlinc-server)

## Installation

```bash
ansible-galaxy collection install git+https://github.com/cendio/ansible-collection-thinlinc.git
```

## Example playbook

```yaml
- name: Configure ThinLinc servers
  hosts: thinlinc_masters:thinlinc_agents
  become: true
  roles:
    - cendio.thinlinc.common
    - role: thinlinc-server
      vars:
        thinlinc_accept_eula: "yes"

- name: Configure ThinLinc agents
  hosts: thinlinc_agents
  become: true
  roles:
    - role: cendio.thinlinc.desktop
      vars:
        desktop_envs: ["mate"]
```

## Roles

| Role | Description |
|------|-------------|
| [common](roles/common/README.md) | Tasks which are generally useful for all ThinLinc servers |
| [desktop](roles/desktop/README.md) | Installs and configures supported desktop environments |

## License

GPL-3.0-or-later

## Author

Cendio AB
