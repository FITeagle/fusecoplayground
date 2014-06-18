```````````````````````````````
Accessing the Nodes via SFA
```````````````````````````````

We assume that you've already valid access credentials (see :ref:`sfaaccess-label`).

.. contents:: Table of Contents


Status of the Testbed
=====================

Check https://flsmonitor.fed4fire.eu to see the status and number of free resources on the Fed4FIRE testbeds, including the FUSECO Playground.


Software Installation
=====================

Conceptionally, it should be possible to request resources using any SFA compliant tool.
One example is the `jFed Probe Tool <http://jfed.iminds.be>`_ (tested with release 1388) and we assume that you've
installed the binary and started it for example via command line::

   java -jar jFed-probe-GUI.jar

Software Configuration
======================

Depending on the used client, you first need to configure the according testbed endpoints:

* SFA Aggregate Manager v3

  * URL: https://fuseco.fokus.fraunhofer.de/api/sfa/am/v3
  * URN: urn:publicid:IDN+fuseco.fokus.fraunhofer.de+authority+root

* SFA User and Slice API: 

  * URL: https://fuseco.fokus.fraunhofer.de/api/sfa/registry/v1
  * URN: urn:publicid:IDN+fuseco.fokus.fraunhofer.de+authority+cm


Resource Descriptions (RSpecs)
==============================

Depending on the result of the listResources call, it is possible to provision different resources.
This documentation gives you simple examples:

Monitored Ubuntu Machine
------------------------

The RSpec Request::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <rspec
    type="request"
    generated="2014-06-13T14:20:39Z"
    xsi:schemaLocation="http://www.geni.net/resources/rspec/3
    http://www.geni.net/resources/rspec/3/request.xsd " 
    xmlns:client="http://www.protogeni.net/resources/rspec/ext/client/1" 
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns="http://www.geni.net/resources/rspec/3">
    <node
      client_id="PC"
      component_manager_id="urn:publicid:IDN+homer+authority+root"
      component_id="urn:publicid:IDN+homer+node+fOpenStack"
      exclusive="true">
      <sliver_type name="m1.tiny">
        <disk_image name="ubuntu-64-with-monitoringScripts"/>
      </sliver_type>
    </node>
  </rspec>

