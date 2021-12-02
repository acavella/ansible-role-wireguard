# Ansible Role: Wireguard

![GitHub last commit](https://img.shields.io/github/last-commit/acavella/ansible-role-wireguard)
![GitHub repo size](https://img.shields.io/github/repo-size/acavella/ansible-role-wireguard)

An Ansible Role that installs and configures Wireguard on Linux.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    wg_version: "1.17.3"
    wg_platform: linux
    wg_arch: amd64

Version, platform, and architecture to use when downloading Go.

    wg_tarball: wg{{ wg_version }}.{{ wg_platform }}-{{ wg_arch }}.tar.gz
    wg_download_url: https://dl.google.com/wg/{{ wg_tarball }}

These two variables are used to build the download URL when installing Go.

    wg_checksum: '550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'

SHA256 checksum of the Go download. If changing the version, platform, or architecture, you will also need to update this checksum, too.

## Dependencies

None.

## Example Playbook

    - hosts: myserver
      roles:
        - { role: geerlingguy.go }

## License

GNU GENERAL PUBLIC LICENSE v3.0

## Author Information

This role was created in 2021 by [Tony Cavella](https://www.cavella.com/)
