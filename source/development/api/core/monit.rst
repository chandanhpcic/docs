Monit
~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","monit","service","configtest",""
    "``POST``","monit","service","reconfigure",""
    "``GET``","monit","service","reconfigure",""
    "``GET``","monit","service","restart",""
    "``GET``","monit","service","start",""
    "``GET``","monit","service","status",""
    "``GET``","monit","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `Monit.xml <https://github.com/reticen8/core/blob/master/src/reticen8/mvc/app/models/Reticen8/Monit/Monit.xml>`__"

.. csv-table:: Resources (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","monit","settings","addAlert",""
    "``POST``","monit","settings","addService",""
    "``POST``","monit","settings","addTest",""
    "``POST``","monit","settings","delAlert","$uuid"
    "``POST``","monit","settings","delService","$uuid"
    "``POST``","monit","settings","delTest","$uuid"
    "``GET``","monit","settings","dirty",""
    "``GET``","monit","settings","get",""
    "``GET``","monit","settings","getAlert","$uuid=null"
    "``GET``","monit","settings","getGeneral",""
    "``GET``","monit","settings","getService","$uuid=null"
    "``GET``","monit","settings","getTest","$uuid=null"
    "``*``","monit","settings","searchAlert",""
    "``*``","monit","settings","searchService",""
    "``*``","monit","settings","searchTest",""
    "``GET``","monit","settings","set",""
    "``POST``","monit","settings","setAlert","$uuid"
    "``POST``","monit","settings","setService","$uuid"
    "``POST``","monit","settings","setTest","$uuid"
    "``POST``","monit","settings","toggleAlert","$uuid,$enabled=null"
    "``POST``","monit","settings","toggleService","$uuid,$enabled=null"

    "``<<uses>>``", "", "", "", "*model* `Monit.xml <https://github.com/reticen8/core/blob/master/src/reticen8/mvc/app/models/Reticen8/Monit/Monit.xml>`__"

.. csv-table:: Resources (StatusController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","monit","status","get","$format='xml'"
