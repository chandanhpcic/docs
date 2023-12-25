Zabbixproxy
~~~~~~~~~~~

.. csv-table:: Service (GeneralController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","zabbixproxy","general","get",""
    "``GET``","zabbixproxy","general","set",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/zabbix-proxy/src/reticen8/mvc/app/models/Reticen8/Zabbixproxy/General.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","zabbixproxy","service","reconfigure",""
    "``GET``","zabbixproxy","service","restart",""
    "``GET``","zabbixproxy","service","start",""
    "``GET``","zabbixproxy","service","status",""
    "``GET``","zabbixproxy","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `General.xml <https://github.com/reticen8/plugins/blob/master/net-mgmt/zabbix-proxy/src/reticen8/mvc/app/models/Reticen8/Zabbixproxy/General.xml>`__"
