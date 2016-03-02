tomcat-8
=======

An ansible role to install tomcat 8 on Debian based distributions.
The installation uses the packages provided with the distribution
and does not download packages (.deb, .tar.gz, ...) from other
repositories.

Requirements
------------

None

Role Variables
--------------

The  variables should be configured by the user (default values provided) :


* ``tomcat_keystore_passphrase``: Keystore and private key passphrase (string, default: ``changeit``)
* ``tomcat_keystore_cert_alias``: Keystore alias for the certifiage (string, default: ``tomcat``)
* ``tomcat_default_port``: Default connector port (integer, default: ``8080``)
* ``tomcat_default_port_ssl``: Default redirect port (integer, default: ``8443``)
* ``tomcat_memory_size``: Tomcat memory size (string, default: ``1024m``)
* ``tomcat_memory_permsize``: Tomcat memory PermSize (string, default: ``128m``)
* ``keystore``: Path to the keystore containing the certificates for the ssl. If undefined a self-signed certificate is generated (path, default: unassigned)

Dependencies
------------

None

Example Playbook
----------------

To use the role you have to add in your playbook:

    - hosts: servers
      roles:
         - osct.tomcat-8

License
-------

Apache v. 2.0

Author Information
------------------

This role was created by [Marco Fargetta](http://fmarco76.github.io) at the [INFN division of Catania](http://www.ct.infn.it) for use with the federation [GrIDP](http://gridp.ct.infn.it).
