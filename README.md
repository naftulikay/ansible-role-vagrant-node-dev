# ansible-role-vagrant-node-dev [![Build Status][travis.svg]][travis]

An Ansible role for a Vagrant-based NodeJS development setup.

Available on Ansible Galaxy at [`naftulikay.vagrant-node-dev`][galaxy].

## Requirements

A Vagrant machine running a supported operating system.

## Role Variables

<dl>
  <dt><code>node_version</code></dt>
  <dd>The version of NodeJS to install.</dd>
  <dt><code>vagrant_user</code></dt>
  <dd>The username of the Vagrant user, defaults to <code>vagrant</code></dd>
</dl>

> Please see the upstream [`naftulikay.vagrant-base`][vagrant-base] and [`naftulikay.node-dev`][node-dev] roles for
additional supported variables.

## Dependencies

 - [`naftulikay.vagrant-base`][vagrant-base]: Provides base Vagrant configuration.
 - [`naftulikay.node-dev`][node-dev]: Provides a basic NodeJS development environment.

## Example Playbook

Install a NodeJS development environment within the Vagrant machine:

```
---
- hosts: all
  roles:
    - role: vagrant-node-dev
      node_version: 6.11.2
```

## LICENSE

MIT.

 [travis]: https://travis-ci.org/naftulikay/ansible-role-vagrant-node-dev
 [travis.svg]: https://travis-ci.org/naftulikay/ansible-role-vagrant-node-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/vagrant-node-dev/
 [vagrant-base]: https://galaxy.ansible.com/naftulikay/vagrant-base/
 [node-dev]: https://galaxy.ansible.com/naftulikay/node-dev/
