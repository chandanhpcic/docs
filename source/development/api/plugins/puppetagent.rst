Puppetagent
~~~~~~~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","puppetagent","service","reconfigure",""
    "``GET``","puppetagent","service","restart",""
    "``GET``","puppetagent","service","start",""
    "``GET``","puppetagent","service","status",""
    "``GET``","puppetagent","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `PuppetAgent.xml <https://github.com/reticen8/plugins/blob/master/sysutils/puppet-agent/src/reticen8/mvc/app/models/Reticen8/PuppetAgent/PuppetAgent.xml>`__"

.. csv-table:: Service (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","puppetagent","settings","get",""
    "``GET``","puppetagent","settings","set",""

    "``<<uses>>``", "", "", "", "*model* `PuppetAgent.xml <https://github.com/reticen8/plugins/blob/master/sysutils/puppet-agent/src/reticen8/mvc/app/models/Reticen8/PuppetAgent/PuppetAgent.xml>`__"
