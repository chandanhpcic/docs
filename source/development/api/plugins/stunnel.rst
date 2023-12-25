Stunnel
~~~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","stunnel","service","reconfigure",""
    "``GET``","stunnel","service","restart",""
    "``GET``","stunnel","service","start",""
    "``GET``","stunnel","service","status",""
    "``GET``","stunnel","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `Stunnel.xml <https://github.com/reticen8/plugins/blob/master/security/stunnel/src/reticen8/mvc/app/models/Reticen8/Stunnel/Stunnel.xml>`__"

.. csv-table:: Service (ServicesController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","stunnel","services","addItem",""
    "``POST``","stunnel","services","delItem","$uuid"
    "``GET``","stunnel","services","get",""
    "``GET``","stunnel","services","get",""
    "``GET``","stunnel","services","getItem","$uuid=null"
    "``*``","stunnel","services","searchItem",""
    "``GET``","stunnel","services","set",""
    "``POST``","stunnel","services","setItem","$uuid"
    "``POST``","stunnel","services","toggleItem","$uuid,$enabled=null"

    "``<<uses>>``", "", "", "", "*model* `Stunnel.xml <https://github.com/reticen8/plugins/blob/master/security/stunnel/src/reticen8/mvc/app/models/Reticen8/Stunnel/Stunnel.xml>`__"
