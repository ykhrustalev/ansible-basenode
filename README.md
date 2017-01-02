Role Name
=========

[![Build Status](https://travis-ci.org/ykhrustalev/ansible-basenode.svg?branch=master)](https://travis-ci.org/ykhrustalev/ansible-basenode)

Basic node, currently debian, keep track on initial setup

Installation
------------

    ansible-galaxy install ykhrustalev.basenode

Requirements
------------

Debian version >= 6

Role Variables
--------------

There are fooloing defaults defined

    ---
    basenode_motd: |
      |                                 |
      |    Server managed by Ansible    |
      |                                 |



    # packages to be installed for debian
    basenode_debian_packages:
      - curl
      - htop
      - iftop
      - iotop
      - openssh-client
      - openssh-server
      - rsync
      - strace
      - sudo
      - tmux
      - unzip
      - vim
      - wget

Role does not use any hardcoded variables
    

Dependencies
------------

None

Example Playbook
----------------

To use add

    - hosts: servers
      roles:
         - role: ykhrustalev.basenode
           basenode_packages:
             - vim

License
-------

MIT

Author Information
------------------

Yuri Khrustalev
