Softether
~~~~~~~~~

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","softether","general","get",""
    "``POST``","softether","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/security/softether/src/reticen8/mvc/app/models/Reticen8/Softether/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","softether","service","reconfigure",""
    "``POST``","softether","service","restart",""
    "``POST``","softether","service","start",""
    "``GET``","softether","service","status",""
    "``POST``","softether","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/security/softether/src/reticen8/mvc/app/models/Reticen8/Softether/General.xml>`__"
