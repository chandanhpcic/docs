Netdata
~~~~~~~

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","netdata","general","get",""
    "``GET``","netdata","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/netdata/src/reticen8/mvc/app/models/Reticen8/Netdata/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","netdata","service","reconfigure",""
    "``GET``","netdata","service","restart",""
    "``GET``","netdata","service","start",""
    "``GET``","netdata","service","status",""
    "``GET``","netdata","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/netdata/src/reticen8/mvc/app/models/Reticen8/Netdata/General.xml>`__"
