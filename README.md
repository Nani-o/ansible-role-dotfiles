[![Build Status](https://travis-ci.org/Nani-o/ansible-role-dotfiles.svg?branch=master)](https://travis-ci.org/Nani-o/ansible-role-dotfiles)

dotfiles
========

This role clone a repository with dotfiles and links them to the current user home.

Compatibility
-------------

  - CentOS 6
  - CentOS 7
  - Ubuntu 14.04
  - Ubuntu 16.04
  - Ubuntu 18.04
  - Debian 8
  - Debian 9

Role Variables
--------------

- dotfiles_git_repo

A git url to the repo holding the dotfiles. [Here](https://github.com/Nani-o/dotfiles) is mine for example.

```YAML
dotfiles_repo: "https://github.com/Nani-o/dotfiles"
```

- dotfiles_clone_path

Path where the repo will be cloned.

```YAML
dotfiles_repo_clone_path: "{{ ansible_user_dir }}/dotfiles"
```

- dotfiles_home_path

Path where the dotfiles will be linked.

```YAML
dotfiles_home_path: "{{ ansible_user_dir }}"
```

Example Playbook
----------------

```YAML
    - hosts: servers
      roles:
         - { role: dotfiles }
```

License
-------

MIT

Author Information
------------------

Sofiane MEDJKOUNE
