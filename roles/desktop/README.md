# cendio.thinlinc.desktop

Install and configure desktop environments for use within a ThinLinc session.

## Requirements

None.

## Role Variables

The following variables are required:

| Variable | Description | Example |
|----------|-------------|---------|
| `desktop_envs` | List of desktop environments to configure | `["mate", "xfce"]` |

## Dependencies

None.

## Usage

```yaml
- name: Install MATE on ThinLinc agent servers
  hosts: thinlinc_agents
  become: true
  roles:
    - role: cendio.thinlinc.desktop
      vars:
        desktop_envs: ["mate"]
```

## License

GPL-3.0-or-later

## Author

Cendio AB
