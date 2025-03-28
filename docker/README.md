Docker
=========

A role to manage docker installation and others operations like start, stop

Requirements
------------

Nothing required

Role Variables
--------------

All actions for docker service :

  <code>action: type string | default("install")</code>
  
    - install
    - remove
    - update
---

All states for docker service :

  <code>state: type string | default("started")</code>
  
    - started
    - stopped
    - reloaded 

---
Enable state for docker at boot 

  <code>enabled: type boolean | default("yes")</code>
  
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
         - { role: docker, trigger_action: install, enable: yes, state: started }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
