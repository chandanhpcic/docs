Vnstat
~~~~~~

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","vnstat","general","get",""
    "``GET``","vnstat","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net/vnstat/src/reticen8/mvc/app/models/Reticen8/Vnstat/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","vnstat","service","daily",""
    "``GET``","vnstat","service","hourly",""
    "``GET``","vnstat","service","monthly",""
    "``GET``","vnstat","service","reconfigure",""
    "``GET``","vnstat","service","resetdb",""
    "``GET``","vnstat","service","restart",""
    "``GET``","vnstat","service","start",""
    "``GET``","vnstat","service","status",""
    "``GET``","vnstat","service","stop",""
    "``GET``","vnstat","service","yearly",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net/vnstat/src/reticen8/mvc/app/models/Reticen8/Vnstat/General.xml>`__"
