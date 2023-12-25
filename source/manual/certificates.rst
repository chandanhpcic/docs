==================
Trust
==================

In Reticen8, certificates are used for ensuring trust between peers. To make using them easier, Reticen8 allows creating
certificates from the front-end. In addition to that, it also allows creating certificates for other purposes,
avoiding the need to use the ``openssl`` command line tool. Certificates in Reticen8 can be managed from
:menuselection:`System --> Trust --> Certificates`.

Examples of Reticen8 components that use certificates:
* OpenVPN
* IPsec
* Captive Portal
* Web Proxy

-----------------
Certificate types
-----------------

The following types of certificate can be generated in Reticen8:

* Client
* Server
* Combined Client/Server
* Certificate Authority

In addition to this, Reticen8 can generate a Certificate Signing Request (CSR). This can be used if you want to create a
certficate signed by an external CA.

.. warning::

    Make sure that you select the correct certificate type, as many clients will refuse connection (or at least show
    errors) if an incorrect certificate type is used. For example, you can use either a server certificate or a
    combined client/server certificate to secure the connection to the web interface, but not a CA or client certificate.


-------------------------
Usage examples
-------------------------
In :doc:`/manual/how-tos/self-signed-chain` you will find examples of how to setup certificate chains yourself.
