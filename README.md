Role Name
=========

An Ansible role for configuring and executing Tempest from and against an
Undercloud.

Requirements
------------

This role assumes it will be executed against a single virthost upon which a
Liberty or Mitaka under/overcloud have been deployed.

Role Variables
--------------

* configure_tempest: <true>  -- Flag which toggles tempest env. setup prior to test execution
* tempest_log_file: <'tempest_output.log'> -- Output file into which Tempest execution output will be added to
* test_regex: <'tempest\.api\.baremetal.*'> -- Regex applied during test execution controlling which tests are executed
* working_dir: <'/home/stack'> -- Location from which Tempest will be configured and executed

Dependencies
------------

n/a

Example Playbook
----------------

    ----
    - name: Test Ironic API baremetal tests
      hosts: undercloud
      roles:
        - ansible-role-tripleo-tempest-undercloud


License
-------

Apache

Author Information
------------------

RDO-CI Team
