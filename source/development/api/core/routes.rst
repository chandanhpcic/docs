Routes
~~~~~~

.. csv-table:: Resources (GatewayController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","routes","gateway","status",""

.. csv-table:: Resources (RoutesController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","routes","routes","addroute",""
    "``POST``","routes","routes","delroute","$uuid"
    "``GET``","routes","routes","get",""
    "``GET``","routes","routes","getroute","$uuid=null"
    "``POST``","routes","routes","reconfigure",""
    "``*``","routes","routes","searchroute",""
    "``GET``","routes","routes","set",""
    "``POST``","routes","routes","setroute","$uuid"
    "``POST``","routes","routes","toggleroute","$uuid,$disabled=null"

    "``<<uses>>``", "", "", "", "*model* `Route.xml <https://github.com/reticen8/core/blob/master/src/reticen8/mvc/app/models/Reticen8/Routes/Route.xml>`__"
