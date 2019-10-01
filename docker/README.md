Docker
=========

A role to manage docker installation and others operations like start, stop

Requirements
------------

Nothing required

Role Variables
--------------
vars:

  - { var: action , type: string }

Select action this list :
  - 'install'
  - 'update'
  - 'start'
  - 'stop'
  - 'remove'
  - 'add_to_boot'

Dependencies
------------

No dependencies.

Example Playbook
----------------

For launch this role :

    - hosts: all
      roles:
         - { role: docker , action: install }
         - { role: docker , action: start }
         - { role: docker , action: add_to_boot }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
