Nut
~~~

.. csv-table:: Resources (DiagnosticsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","nut","diagnostics","upsstatus",""

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","nut","service","reconfigure",""
    "``GET``","nut","service","restart",""
    "``GET``","nut","service","start",""
    "``GET``","nut","service","status",""
    "``GET``","nut","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `Nut.xml <https://github.com/reticen8/plugins/blob/master/sysutils/nut/src/reticen8/mvc/app/models/Reticen8/Nut/Nut.xml>`__"

.. csv-table:: Service (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","nut","settings","get",""
    "``GET``","nut","settings","set",""

    "``<<uses>>``", "", "", "", "*model* `Nut.xml <https://github.com/reticen8/plugins/blob/master/sysutils/nut/src/reticen8/mvc/app/models/Reticen8/Nut/Nut.xml>`__"
