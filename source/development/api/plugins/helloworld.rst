Helloworld
~~~~~~~~~~

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","helloworld","service","reload",""
    "``POST``","helloworld","service","test",""

.. csv-table:: Resources (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","helloworld","settings","get",""
    "``POST``","helloworld","settings","set",""

.. csv-table:: Service (SimplifiedSettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","helloworld","simplified_settings","get",""
    "``GET``","helloworld","simplified_settings","set",""

    "``<<uses>>``", "", "", "", "*model* `HelloWorld.xml <https://github.com/reticen8/plugins/blob/master/devel/helloworld/src/reticen8/mvc/app/models/Reticen8/HelloWorld/HelloWorld.xml>`__"
