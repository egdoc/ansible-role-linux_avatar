Ansible Role: linux_avatar
==================

[![CI](https://github.com/egdoc/ansible-role-linux_avatar/actions/workflows/ci.yml/badge.svg)](https://github.com/egdoc/ansible-role-linux_avatar/actions/workflows/ci.yml)

Ansible role to setup user avatars on Linux workstations.

Requirements
-------------
Requires the ansible community.general collection

Role Variables
--------------
        linux_avatar_users: []

A list of dictionaries specifying usernames and their respective avatar URLs (see example playbook).
User accounts must exist, this role won't create them.

        linux_avatar_icon_dir: /var/lib/AccountsService/icons

The directory holding user avatars

        linux_avatar_user_dir: /var/lib/AccountsService/users

The directory holding the AccountsService user profile configuration

Dependencies
------------
None

Example Playbook
----------------

    - hosts: workstations
      roles:
        - role: egdoc.linux_avatar
          linux_avatar_users:
            - url: https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png
              username: octocat

License
-------

GPLv2

Author Information
------------------
Created by Egidio Docile
