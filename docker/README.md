Docker
=========

A role to manage docker installation and others operations like start, stop

Requirements
------------

Nothing required

Role Variables
--------------

All actions for docker service :

  <code>action: type string</code>
  
    - install
    - remove
    - update
---

All states for docker service :

  <code>state: type string</code>
  
    - started
    - stopped
    - reloaded 
---
Enable state for docker at boot 

  <code>action: type boolean</code>
  
    - yes
    - no
          
Dependencies
------------

No dependencies.

Example Playbook
----------------

For launch this role :

    - hosts: all
      roles:
         # This call will install, start and enable docker at boot
         - { role: docker , action: install , enable: true , state: started , user_docker: < Your_user > }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
