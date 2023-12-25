Openconnect
~~~~~~~~~~~

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","openconnect","general","get",""
    "``POST``","openconnect","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/security/openconnect/src/reticen8/mvc/app/models/Reticen8/Openconnect/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","openconnect","service","reconfigure",""
    "``POST``","openconnect","service","restart",""
    "``POST``","openconnect","service","start",""
    "``GET``","openconnect","service","status",""
    "``POST``","openconnect","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/security/openconnect/src/reticen8/mvc/app/models/Reticen8/Openconnect/General.xml>`__"
