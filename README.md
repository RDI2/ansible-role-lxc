# Ansible Role - lxc

This role installs [LXC](https://linuxcontainers.org/).

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

## Creating a container

```bash
# Create CentOS 7 container as cn01
lxc-create -n cn01 -t centos -- --release 7

# Start cn01 container
lxc-start -d -n cn01

# Connect console via tty0. Somehow the default, tty1
# doesn't work properly in my test.
lxc-console -n cn01 -t 0

# Stop cn01
lxc-stop -n cn01
```

## License

MIT License.

## Author

- Koji Tanaka, RDI2
