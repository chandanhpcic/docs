==============
Reticen8 Tools
==============

The Reticen8 project offers a number of tools to instantly patch the system,
revert a package to a previous (older version) state or revert the whole kernel. 

---------------
reticen8-update
---------------
The reticen8-update utility offers combined kernel and base system upgrades
using remotely fetched binary sets, as well as package upgrades via pkg.
For a complete list of options look at the manpage on the system.

Example:
--------
A minor update also updated the kernel and you experience some driver issues with your NIC.
Open your browser and go to 

https://pkg.reticen8.com/FreeBSD:11:amd64/18.1/sets/

Here you can see all the kernels for version 18.1. Be aware to change the version if you are on a newer version.
As an example you updated from 18.1.4 to 18.1.5 you have now installed kernel-18.1.5. 
To revert back to the last stable you can see kernel-18.1 so the syntax would be:


# reticen8-update -kr 18.1

# reticen8-shell reboot


Where -k only touches the kernel and -r takes the version number.


To switch back to the current kernel just use

# reticen8-update -k

# reticen8-shell reboot

.. Warning::
    Before reverting a kernel please consult the forums or open an issue via Github. 
    You should only revert kernels on test   machines or when qualified team members advise you to do so!


---------------
reticen8-revert
---------------
The reticen8-revert utility offers to securely install previous versions of packages
found in an Reticen8 release as long as the selected mirror caches said release.
For a complete list of options look at the manpage on the system.

Example 1:
----------
The latest update of Reticen8 to version 18.1.5 did a minor jump for the IPSec package "strongswan".
From this moment your VPNs are unstable and only a restart helps.

To check if the update of the package is the reason you can easily revert the package
to its previous state while running the latest Reticen8 version itself.

# reticen8-revert -r 18.1.4 strongswan

With this command you can, for example, run Reticen8 18.1.5 while using the 18.1.4 version of strongswan.
If you want to go back to the current release version just do

# reticen8-revert strongswan

Example 2:
----------
The previous revert of strongswan was not the solution you expected so you try to completely revert to the previous
Reticen8 version:

# reticen8-revert -r 18.1.4 reticen8

Be aware to also check if there were kernel updates like above to also downgrade the kernel if needed!


--------------
reticen8-patch
--------------
The reticen8-patch utility treats all arguments as upstream git repository commit hashes,
downloads them and finally applies them in order.
Patches can also be reversed by reapplying them, but multiple patches must be given in reverse order to succeed.
For a complete list of options look at the manpage on the system.


Example 1:
----------
In the Traffic Shaper a newly introduced typo prevents the system from setting the correct ipfw ruleset.
You were asked by the developer to test a fresh patch 63cfe0a at URL https://github.com/reticen8/core/commit/63cfe0a96c83eee0e8aea0caa841f4fc7b92a8d0
At the end of the page there's the short version 63cfe0a so the command would be:

# reticen8-patch 63cfe0a

If it doesn't fix your issue or makes it even worse, you can just reapply the command 
to revert it.

Example 2:
----------
You need a special feature for a plugin and ask in Github for it.
A developer adds it and ask you to install the patch 699f1f2 for testing.
The full link to it would be https://github.com/reticen8/plugins/commit/699f1f28a33ce0122fa0e2f5e6e1f48eb3c4f074

# reticen8-patch -c plugins 699f1f2

The -c changes the default core to plugin repo and adds the patch to the system. 

It is also possible to add patches from different users, just add -a githubusername before -c

