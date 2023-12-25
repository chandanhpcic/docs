Redis
~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","redis","service","reconfigure",""
    "``GET``","redis","service","resetdb",""
    "``GET``","redis","service","restart",""
    "``GET``","redis","service","start",""
    "``GET``","redis","service","status",""
    "``GET``","redis","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `Redis.xml <https://github.com/reticen8/plugins/blob/master/databases/redis/src/reticen8/mvc/app/models/Reticen8/Redis/Redis.xml>`__"

.. csv-table:: Service (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","redis","settings","get",""
    "``GET``","redis","settings","set",""

    "``<<uses>>``", "", "", "", "*model* `Redis.xml <https://github.com/reticen8/plugins/blob/master/databases/redis/src/reticen8/mvc/app/models/Reticen8/Redis/Redis.xml>`__"
