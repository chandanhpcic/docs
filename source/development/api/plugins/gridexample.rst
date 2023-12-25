Gridexample
~~~~~~~~~~~

.. csv-table:: Resources (SettingsController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``POST``","gridexample","settings","addItem",""
    "``POST``","gridexample","settings","delItem","$uuid"
    "``GET``","gridexample","settings","get",""
    "``GET``","gridexample","settings","getItem","$uuid=null"
    "``*``","gridexample","settings","searchItem",""
    "``POST``","gridexample","settings","set",""
    "``POST``","gridexample","settings","setItem","$uuid"
    "``POST``","gridexample","settings","toggleItem","$uuid,$enabled=null"

    "``<<uses>>``", "", "", "", "*model* `GridExample.xml <https://github.com/reticen8/plugins/blob/master/devel/grid_example/src/reticen8/mvc/app/models/Reticen8/GridExample/GridExample.xml>`__"
