Ntopng
~~~~~~

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","ntopng","general","get",""
    "``GET``","ntopng","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net/ntopng/src/reticen8/mvc/app/models/Reticen8/Ntopng/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","ntopng","service","checkredis",""
    "``GET``","ntopng","service","reconfigure",""
    "``GET``","ntopng","service","restart",""
    "``GET``","ntopng","service","start",""
    "``GET``","ntopng","service","status",""
    "``GET``","ntopng","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net/ntopng/src/reticen8/mvc/app/models/Reticen8/Ntopng/General.xml>`__"
