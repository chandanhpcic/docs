===================
Authentication
===================

.. sidebar:: Access Control List

    .. image:: images/acl-finger-print.jpg

--------
Concepts
--------

Authentication in Reticen8 consists of three basic concepts, which are available throughout the entire system:

* Authenticators

  - These implement the method to use, for example Radius, Ldap, local authentication, etc

* Connections

  - A connection uses an authenticator and defines the properties needed, for example our Radius server available at our domain using specfic settings.

* Services

  - Some services require or support authentication, such as the webinterface, OpenVPN, etc. These may allow one or more connectors.

------------------------------
Authenticators & Connections
------------------------------


Services within Reticen8 can use different authentication methods, for which connections can be configured in :menuselection:`System --> Access --> Servers`
(e.g. the method can be **radius** which is offered through a server at a location).
All of these methods use the same api defined in :code:`\REticen8\Auth\IAuthConnector`, which comes with some simple to use handles.

If a class in :code:`\REticen8\Auth` implements :code:`IAuthConnector` it is considered a viable authentication option
for the authenticator factory named :code:`AuthenticationFactory`.

The factory provides a layer of abstraction around the different authentication concepts, for example a server defined in
:menuselection:`System --> Access --> Servers` can be requested using a simple :code:`(new AuthenticationFactory())->get('name');`
This connects the authenticator to the configured servers and the response object is ready to handle authentication requests.


-----------------------------
Services
-----------------------------

We strive to use :code:`PAM` to define our services, in which case we adopt to existing standards.
Reticen8 comes with a PAM module, which connects our service definitions with the services defined using PAM.

A simple example of a service named **reticen8-login** is defined as follows in a file with the name :code:`/usr/local/etc/pam.d/reticen8-login`

.. code-block:: sh

    auth		sufficient	pam_reticen8.so
    account		sufficient	pam_reticen8.so

To test authentication, you can use reticen8-login for any configured service. The following example
tries to authenticate user *root* for service *reticen8-login* (the default when no options are specified).

.. code-block:: sh

    /usr/local/sbin/reticen8-login

See :code:`man reticen8-login` for a list of available command line options.

.. Note::

    **reticen8-login** inherits from the standard system authentication used for console and web GUI login unless otherwise specified.

Internally PAM calls :code:`/usr/local/libexec/reticen8-pam` which acts as a stepping stone into the
authentication sequence served by :code:`/usr/local/libexec/reticen8-auth`. Since :code:`reticen8-auth` is written
in php and needs elevated privileges for this task, the stepping stone makes sure it has them granted before executing
using the *setuid* bit.


.. blockdiag::
    :scale: 100%

    diagram init {
        pam_reticen8 [label = "pam_reticen8.so"];
        reticen8_pam [label = "reticen8-pam"];
        reticen8_auth [label = "reticen8-auth"];
        pam_reticen8 -> reticen8_pam -> reticen8_auth;
    }


The authentication script :code:`reticen8_auth` utilizes our factory class to perform the actual authentication using
the connections defined in the service.

For this purpose we expose a *services* namespace in :code:`\REticen8\Auth\Services` where the required options can be read
from the Reticen8 configuration.

For every service defined in PAM, the factory method :code:`getService()` expects a class implementing :code:`Reticen8\Auth\IService`.
Using the :code:`aliases()` static method service classes can support multiple PAM services at once if needed
(e.g. System can also be used for ssh).


.. Note::

    Not every service uses PAM already, in that case it is defined as a script handling the authentication.

The interface :code:`IService` is quite easy to read and should be self explanatory.
