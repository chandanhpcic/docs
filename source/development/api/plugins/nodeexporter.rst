Nodeexporter
~~~~~~~~~~~~

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","nodeexporter","general","get",""
    "``GET``","nodeexporter","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/sysutils/node_exporter/src/reticen8/mvc/app/models/Reticen8/NodeExporter/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","nodeexporter","service","reconfigure",""
    "``GET``","nodeexporter","service","restart",""
    "``GET``","nodeexporter","service","start",""
    "``GET``","nodeexporter","service","status",""
    "``GET``","nodeexporter","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/sysutils/node_exporter/src/reticen8/mvc/app/models/Reticen8/NodeExporter/General.xml>`__"
