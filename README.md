Debian Docker Toolbox
=========

<!--
A brief description of the role goes here.
-->
Provisioning dev machines with the Docker Toolbox
  * docker-engine
  * docker-machine
  * docker-compose

Requirements
------------

<!--
Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.
-->
None

Role Variables
--------------

<!--
A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.
-->
* `docker_compose_version` - the current version of Docker Compose that's being installed
* `docker_engine_version` - version of Docker Engine that ought to be installed (use the full debian version)
* `docker_repo` - Docker Repository available to add in Debian APT Registry:
  * `stable` - reliable updates every quarter
  * `edge` - new features monthly

Dependencies
------------

<!--
A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.
-->
None

Example Playbook
----------------

<!--
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }
-->
```yml
- hosts: local
  roles:
    - { role: ansible-roles.debian-docker-toolbox,
        docker_repo: edge }
```

License
-------

GPLv3

Author Information
------------------

<!--
An optional section for the role authors to include contact information, or a website (HTML is not allowed).
-->
Daniel Andrei Minca <dminca@protonmail.com>
