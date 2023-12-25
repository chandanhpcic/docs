Zabbixagent
~~~~~~~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","zabbixagent","service","reconfigure",""
    "``GET``","zabbixagent","service","restart",""
    "``GET``","zabbixagent","service","start",""
    "``GET``","zabbixagent","service","status",""
    "``GET``","zabbixagent","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `ZabbixAgent.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/zabbix-agent/src/reticen8/mvc/app/models/Reticen8/ZabbixAgent/ZabbixAgent.xml>`__"

.. csv-table:: Resources (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","zabbixagent","settings","addAlias",""
    "``POST``","zabbixagent","settings","addUserparameter",""
    "``POST``","zabbixagent","settings","delAlias","$uuid"
    "``POST``","zabbixagent","settings","delUserparameter","$uuid"
    "``GET``","zabbixagent","settings","get",""
    "``GET``","zabbixagent","settings","getAlias","$uuid=null"
    "``GET``","zabbixagent","settings","getUserparameter","$uuid=null"
    "``*``","zabbixagent","settings","searchAliases",""
    "``*``","zabbixagent","settings","searchUserparameters",""
    "``GET``","zabbixagent","settings","set",""
    "``POST``","zabbixagent","settings","setAlias","$uuid"
    "``POST``","zabbixagent","settings","setUserparameter","$uuid"
    "``POST``","zabbixagent","settings","toggleAlias","$uuid"
    "``POST``","zabbixagent","settings","toggleUserparameter","$uuid"

    "``<<uses>>``", "", "", "", "*model* `ZabbixAgent.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/zabbix-agent/src/reticen8/mvc/app/models/Reticen8/ZabbixAgent/ZabbixAgent.xml>`__"
