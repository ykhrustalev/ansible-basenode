Role Name
=========

Basic node, currently debian, keep track on initial setup

Requirements
------------

Debian version >= 6

Role Variables
--------------

    basenode_locale_list:
      - en_US.UTF-8


    basenode_ssh_users:
      - name: '{{ ansible_ssh_user }}'
        key: ssh-rsa xxx235hash admin

Dependencies
------------

    dependencies:
      - role: ssh
      - role: franklinkim.sudo
      - role: bennojoy.ntp
      - role: Stouts.timezone

Example Playbook
----------------

To use add

    - hosts: servers
      roles:
         - role: ykhrustalev.basenode

License
-------

MIT

Author Information
------------------

Yuri Khrustalev
