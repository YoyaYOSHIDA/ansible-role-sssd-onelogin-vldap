Role Name
=========

Ansible role to setup and enable SSSD client for OneLogin VLDAP(Virtual LDAP)

Requirements
------------

Currently supporting `CentOS7`, `RHEL7` and `AmazonLinux2`. `CentOS8` and `RHEL8` will be supported in time.

Role Variables
--------------

- `ansible_role_sssd_onelogin_vldap_ONELOGIN_SUBDOMAIN`
    - Sub domain of your OneLogin account
- `ansible_role_sssd_onelogin_vldap_ONELOGIN_GIDNUMBER`
    - gidNumber of your OneLogin account
    - See https://gist.github.com/YoyaYOSHIDA/fdd14c712aa0e308b5a3fd72722a02a0#add-onelogin-gidnumber-to-etc-group
- `ansible_role_sssd_onelogin_vldap_ONELOGIN_GROUPNAME`
    - Group name counterpart to gidNumber (Define as you want)
- `ansible_role_sssd_onelogin_vldap_PRIVILEGED_USER_CN`
    - cn of the default bind DN
    - See https://gist.github.com/YoyaYOSHIDA/fdd14c712aa0e308b5a3fd72722a02a0#create-and-edit-sssd-conf
- `ansible_role_sssd_onelogin_vldap_LDAP_DEFAULT_AUTHTOK`
    - The authentication token of the default bind DN

Dependencies
------------

None.

Example Playbook
----------------

- hosts: all
  become: true
  roles:
    - ansible-role-sssd-onelogin-vldap

License
-------

BSD

Author Information
------------------

YoyaYOSHIDA(https://github.com/YoyaYOSHIDA)

