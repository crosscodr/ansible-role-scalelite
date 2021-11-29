Ansible Role Scalelite
=========

Install and configure scalelite loadbalancer for BigBlueButton.

Requirements
------------

This role works with scalelite v1.3 and above!
Docker python sdk must be present.

Role Variables
--------------



Dependencies
------------



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers

      tasks:
      - name: Install Docker
        import_role: 
          name: geerlingguy.docker

      - name: Install docker python sdk
        import_role:
          name: geerlingguy.pip
        vars:
          pip_install_packages:
            - name: docker
            - name: docker-compose
        tags: 
          - docker
          - scalelite-docker

      - name: Deploy scalelite load balancer
        import_role: { name: scalelite }
        tags: scalelite-app


License
-------

BSD
