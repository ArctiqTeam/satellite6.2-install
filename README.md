satellite6.2-install
=========

This role can be called in a playbook to install the Satellite 6.2 packages on a host system.

Requirements
------------

RHEL7 Host to install the packages.  Appropriate system requirements for the Satellite install
The target host needs to be unregistered to any subscription management application (Portal, Satelllite, etc)
A subscription manifest needs to be previously created and downloaded from access.redhat.com ... this manifest needs to be placed in file/manifest.zip for the role to function properly.

Role Variables
--------------

Role Defaults should be edited accordingly.
Be sure to set the following variables ... either prompted or through an extra_vars.yml file:  {{ rhn_username }} {{ rhn_password }}
These get used to register the system to Red Hat and the password is used for the initial Satellite install.

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: satellite
      roles:
         - { role: satellite6.2-install, satellite_org: ABC, satellite_loc: Toronto }

License
-------

GNU GENERAL PUBLIC LICENSE
