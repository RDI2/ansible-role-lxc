# Ansible Role - lxc

This playbook installs [LXC](https://linuxcontainers.org/).

## Platforms

CentOS 7 is the only platform that is supported and tested so far.

## Role Variables

- Check out [defaults/main.yml](defaults/main.yml)

## Dependencies

None.

## Installation

Regular installation:

```
ansible-galaxy install RDI2.lxc
```

Installation to a specific directory(e.g. roles/):

```
ansible-galaxy install -p roles/ RDI2.lxc
```

## Example Playbook

    - hosts: servers
      roles:
         - { role: RDI2.lxc }

## License

MIT License.

## Author

- Koji Tanaka, RDI2
