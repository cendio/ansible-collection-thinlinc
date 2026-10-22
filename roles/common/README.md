# cendio.thinlinc.common

Perform common configuration tasks for setting up a ThinLinc server.

## Requirements

None.

## Role Variables

None.

## Dependencies

None.

## Usage

```yaml
- name: Prepare servers for ThinLinc
  hosts: thinlinc_masters:thinlinc_agents
  become: true
  roles:
    - role: cendio.thinlinc.common
```

## License

GPL-3.0-or-later

## Author

Cendio AB
