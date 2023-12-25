Puppetagent
~~~~~~~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","puppetagent","service","reconfigure",""
    "``POST``","puppetagent","service","restart",""
    "``POST``","puppetagent","service","start",""
    "``GET``","puppetagent","service","status",""
    "``POST``","puppetagent","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `PuppetAgent.xml <https://github.com/reticen8/plugins/blob/master/sysutils/puppet-agent/src/reticen8/mvc/app/models/Reticen8/PuppetAgent/PuppetAgent.xml>`__"

.. csv-table:: Service (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","puppetagent","settings","get",""
    "``POST``","puppetagent","settings","set",""

    "``<<uses>>``", "", "", "", "*model* `PuppetAgent.xml <https://github.com/reticen8/plugins/blob/master/sysutils/puppet-agent/src/reticen8/mvc/app/models/Reticen8/PuppetAgent/PuppetAgent.xml>`__"
