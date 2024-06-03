Ansible Role: tmux
=========

Installs an opinionated tmux configuration under the current user for Linux servers, installing the `tmux` package if it isn't present.
Installs the configuration into `~/.config/tmux` if the current `tmux` version supports it, otherwise installing into `~`.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values:
```yaml
use_vi_keys: true

# number of lines to store in scrollback
history_limit: 75000

# change prefix to C-a to make nested tmux more convenient
tmux_prefix: C-a

# binds C-n and C-p for navigating forward/backward between windows, allowing
# you to hold Ctrl while hitting the prefix key and the navigation key
bind_window_ctrl_nav_keys: true
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
