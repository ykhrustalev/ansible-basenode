Role Name
=========

Basic node, currently debian, keep track on initial setup

Installation
------------

    ansible-galaxy install ykhrustalev.basenode

Requirements
------------

Debian version >= 6

Role Variables
--------------

To install repos list, define

    basenode_codename: jessie
    basenode_install_repos: true


Setup locales

    basenode_locale_list:
      - en_US.UTF-8

SSH access

    basenode_ssh_users:
      - user: '{{ ansible_ssh_user }}'
        key: 'ssh-rsa xxx235hash admin'
        
Sudoers
        
    sudo_users:
      - { name: '%vagrant', nopasswd: yes }
    

Dependencies
------------

    dependencies:
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
