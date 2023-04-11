OpenStack Repo installer
=========

This role installs the OpenStack repository on a ubuntu server.

This role based on the matrix from [OpenStack](https://docs.openstack.org/install-guide/environment-packages-ubuntu.html)

By default, the role installs the default repo for the current ubuntu version so no action is make if you don't specify a repo name.

Requirements
------------

A server with ubuntu and admin access.

gather_facts must be set to true.

Only ubuntu 22.04, 20.04 and 18.04 is supported for now. Feel free to add support for other distros.

Role Variables
--------------

Only one variable is needed: `openstack_repo_name`

Repo name can be one of the following:

- antelope
- zed
- yoga (default for ubuntu 22.04)
- xena
- wallaby
- victoria
- ussuri (default for ubuntu 20.04)
- train
- stein
- rocky
- queens (default for ubuntu 18.04)

Dependencies
------------

No dependencies.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
      - { role: msterhuj.openstack_repo, openstack_repo_name: "antelope" }
```

License
-------

BSD

Author Information
------------------

@msterhuj <gabin.lanore@gmail.com>
