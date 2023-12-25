Rspamd
~~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","rspamd","service","reconfigure",""
    "``POST``","rspamd","service","restart",""
    "``POST``","rspamd","service","start",""
    "``GET``","rspamd","service","status",""
    "``POST``","rspamd","service","stop",""

    "``<<uses>>``", "", "", "", "*model* `RSpamd.xml <https://github.com/reticen8/plugins/blob/master/mail/rspamd/src/reticen8/mvc/app/models/Reticen8/Rspamd/RSpamd.xml>`__"

.. csv-table:: Service (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","rspamd","settings","get",""
    "``POST``","rspamd","settings","set",""

    "``<<uses>>``", "", "", "", "*model* `RSpamd.xml <https://github.com/reticen8/plugins/blob/master/mail/rspamd/src/reticen8/mvc/app/models/Reticen8/Rspamd/RSpamd.xml>`__"
