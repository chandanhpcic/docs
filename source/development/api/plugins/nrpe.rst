Nrpe
~~~~

.. csv-table:: Resources (CommandController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","nrpe","command","addCommand",""
    "``POST``","nrpe","command","delCommand","$uuid"
    "``GET``","nrpe","command","get",""
    "``GET``","nrpe","command","getCommand","$uuid=null"
    "``*``","nrpe","command","searchCommand",""
    "``GET``","nrpe","command","set",""
    "``POST``","nrpe","command","setCommand","$uuid"
    "``POST``","nrpe","command","toggleCommand","$uuid"

    "``<<uses>>``", "", "", "", "*model* `Command.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/nrpe/src/reticen8/mvc/app/models/Reticen8/Nrpe/Command.xml>`__"

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","nrpe","general","get",""
    "``GET``","nrpe","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/nrpe/src/reticen8/mvc/app/models/Reticen8/Nrpe/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","nrpe","service","reconfigure",""
    "``GET``","nrpe","service","restart",""
    "``GET``","nrpe","service","start",""
    "``GET``","nrpe","service","status",""
    "``GET``","nrpe","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/nrpe/src/reticen8/mvc/app/models/Reticen8/Nrpe/General.xml>`__"
