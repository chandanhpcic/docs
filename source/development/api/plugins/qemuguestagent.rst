Qemuguestagent
~~~~~~~~~~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","qemuguestagent","service","reconfigure",""
    "``GET``","qemuguestagent","service","restart",""
    "``GET``","qemuguestagent","service","start",""
    "``GET``","qemuguestagent","service","status",""
    "``GET``","qemuguestagent","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `QemuGuestAgent.xml <https://github.com/reticen8/plugins/blob/master/emulators/qemu-guest-agent/src/reticen8/mvc/app/models/Reticen8/QemuGuestAgent/QemuGuestAgent.xml>`__"

.. csv-table:: Service (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","qemuguestagent","settings","get",""
    "``GET``","qemuguestagent","settings","set",""

    "``<<uses>>``", "", "", "", "*model* `QemuGuestAgent.xml <https://github.com/reticen8/plugins/blob/master/emulators/qemu-guest-agent/src/reticen8/mvc/app/models/Reticen8/QemuGuestAgent/QemuGuestAgent.xml>`__"
