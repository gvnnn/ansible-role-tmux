gvnnn.tmux
==========

Installs and configures tmux

Requirements
------------

None.

Role Variables
--------------

    tmux_conf_template_file: tmux.conf.j2

To provide your own configuration file create a `templates/` directory at the playbook level and override this variable with the name of the template. e.g.:

    mdkir templates
    touch templates/mytmux.conf.j2
    echo "tmux_conf_template_file: mytmux.conf.j2" >> vars/main.yml  # set vars_files accordingly in your playbook

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: workstation
      roles:
         - { role: gvnnn.tmux, tmux_conf_template_file: mytmux.conf.j2 }

License
-------

MIT
