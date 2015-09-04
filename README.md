Ansible nginx-uwsgi-supervisor
==============================

This role is to setup an nginx-uwsgi-supervisor application.  Currently,
this role houses roles from [https://github.com/ryankanno/ansible-roles](https://github.com/ryankanno/ansible-roles), but
at some point down the road, there may be additional tasks added to it.  The
goal for this role is to make said infrastructure less magical to setup and install.

Dependencies
------------

  * [ansible 1.9+](https://github.com/ansible/ansible)
  * [nginx](https://github.com/ryankanno/ansible-roles/tree/master/nginx)
  * [uwsgi](https://github.com/ryankanno/ansible-roles/tree/master/uwsgi)
  * [supervisor](https://github.com/ryankanno/ansible-roles/tree/master/supervisor)

This role is ideally designed to work against a modern Ubuntu / Debian system. It's
only been tested against 14.04 because some of the role dependencies haven't
been updated with instructions for various OSes.

Usage
-----

* clone [https://github.com/ryankanno/ansible-roles](https://github.com/ryankanno/ansible-roles).
* create an ansible.cfg file that has a modified roles_path pointing to where
  you checked out ansible-roles to as well as this role.

Author
------

Ryan Kanno

License
-------

MIT
