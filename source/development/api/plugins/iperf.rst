Iperf
~~~~~

.. csv-table:: Service (InstanceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","iperf","instance","get",""
    "``GET``","iperf","instance","query",""
    "``GET``","iperf","instance","set",""
    "``POST``","iperf","instance","set",""

    "``<<uses>>``", "", "", "", "*model* `FakeInstance.xml <https://github.com/reticen8/plugins/blob/master/benchmarks/iperf/src/reticen8/mvc/app/models/Reticen8/iperf/FakeInstance.xml>`__"

.. csv-table:: Service (ServiceController.php)
   :header: "Method", "Module", "Controller", "Command", "Parameters"
   :widths: 4, 15, 15, 30, 40

    "``GET``","iperf","service","restart",""
    "``GET``","iperf","service","start",""
    "``GET``","iperf","service","status",""
    "``GET``","iperf","service","stop",""
