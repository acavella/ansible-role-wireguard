# Ansible Role: Wireguard
Installs Wireguard VPN on Linux systems.

![GitHub last commit](https://img.shields.io/github/last-commit/acavella/ansible-role-wireguard?style=flat-square)
![GitHub repo size](https://img.shields.io/github/repo-size/acavella/ansible-role-wireguard?style=flat-square)

An Ansible Role that installs and configures Wireguard on Linux.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    go_version: "1.17.3"
    go_platform: linux
    go_arch: amd64

Version, platform, and architecture to use when downloading Go.

    go_tarball: go{{ go_version }}.{{ go_platform }}-{{ go_arch }}.tar.gz
    go_download_url: https://dl.google.com/go/{{ go_tarball }}

These two variables are used to build the download URL when installing Go.

    go_checksum: '550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'

SHA256 checksum of the Go download. If changing the version, platform, or architecture, you will also need to update this checksum, too.

## Dependencies

None.

## Example Playbook

    - hosts: myserver
      roles:
        - { role: geerlingguy.go }

## License

GPLv3

## Author Information

This role was created in 2021 by [Tony Cavella](https://www.cavella.com/)
