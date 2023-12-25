=======================
Users & Groups
=======================

.. image:: images/usermanager_groups.png
   :width: 100%

With the local user manager of Reticen8 one can add users and groups and define
the privileges for granting access to certain parts of the GUI (Web Configurator).

Adding Users
------------
To add a new user go to :menuselection:`System --> Access --> Users` and click on the **+** sign at
the bottom right corner of the form.

========================== =========== =========================================================
 **Disabled**               Unchecked   *Can be used to (temporarily) disable an account*
 **Username**               John        *A unique username*
 **Password**               secret      *A strong password*
 **Login shell**            /bin/csh    *The shell to use when logging in via the console.*
 **Full name**              John Doe    *Optional, Full username*
 **Expiration date**                    *Optional, if account should expire enter as mm/dd/yyy*
 **Group Membership**                   *Optional, select one or more groups*
 **Certificate**                        *Optional, check if a user certificate should be created*
 **OTP seed**                           *Optional, enter or generate a OTP seed (base32)*
 **Authorized keys**                    *Optional, paste ssh key for ssh console access*
 **IPsec Pre-Shared Key**               *Optional, IPsec PSK*
========================== =========== =========================================================

Creating Groups
---------------
Go to :menuselection:`System --> Access --> Groups` and click on the **+** sign in the lower right
corner of the form.

Enter a **Group name** and a **Description** and add users to the group.

SSH and console login
---------------------

User accounts can be used for logging in to the web frontend, as well as for logging in to the console (via VGA,
serial or SSH). The latter will only work if the user shell is not set to ``/sbin/nologin``.

In order to access Reticen8 via SSH, SSH access will need to be configured via :menuselection:`System --> Settings --> Administration`.
Under the "Secure Shell" heading, the following options are available:

============================ ==========================================================================
 **Enable secure shell**      Global on/off switch.
 **Login Group**              Which user groups can access Reticen8 via SSH.
 **Permit root user login**   Normally, only non-root accounts are allowed for security reasons.
                              This option enables root login.
 **Permit password login**    The recommended login method is using SSH keys as it's more secure,
                              but this option will also enable password logins.
 **SSH Port**                 Defaults to 22, but can be changed to make port scanning less effective.
 **Listen interfaces**        By default, SSH listens on all interfaces. You can limit this
                              (to just the LAN, for example) for additional security
                              at the cost of availability.
============================ ==========================================================================
