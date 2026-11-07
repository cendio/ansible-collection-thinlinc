# cendio.thinlinc.gpu

Configure ThinLinc servers for use with a GPU.

## Requirements

None.

## Role Variables

None.

## Dependencies

None.

## Usage

```yaml
- name: Configure agents for GPU usage
  hosts: thinlinc_agents
  become: true
  roles:
    - role: cendio.thinlinc.gpu
```

## License

GPL-3.0-or-later

## Author

Cendio AB
