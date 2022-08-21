mtik00.desk
===========

Install and configure the (https://github.com/jamesob/desk)[desk] CLI tool.

Requirements
------------

This role has no requirements other than ansible.

Role Variables
--------------

Varables are defined in `default.main.yml`:
* `apt_cache_valid_time`: How long the apt cache is valid for (needed to install `git`)
* `binary_dir`: The directory to place a symlink to the `desk` binary
* `binary_dir_mode`: The mode to apply to `binary_dir`
* `clone_dir`: The directory in which to clone the `desk` repository
* `update_desk_clone`: Whether or not to update the cloned folder
* `desk_version`: The `git` tag of the Desk repo to clone
* `install_completions_zsh`: Whether or not to install auto-completions into zsh
* `install_completions_oh_my_zsh`: Whether or not to install auto-completions into oh-my-zsh
* `install_completions_bash`: Whether or not to install auto-completions into bash

Dependencies
------------

This role has no dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: mtik00.desk, install_completions_oh_my_zsh: true }

License
-------

MIT
