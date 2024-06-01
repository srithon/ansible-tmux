Role Name
=========

Installs an opinionated tmux configuration under the current user for Linux servers, installing the `tmux` package if it isn't present.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values:
```yaml
use_vi_keys: false

# number of lines to store in scrollback
history_limit: 75000

# by default, use tmux's stock prefix
tmux_prefix: C-b
```

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: srithon.tmux
           use_vi_keys: true
           tmux_prefix: C-a

License
-------

BSD

Author Information
------------------

This role was created in 2024 by [Sridaran Thoniyil](github.com/srithon).