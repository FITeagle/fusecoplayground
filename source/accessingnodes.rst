```````````````````````````````
Accessing the Nodes via SFA
```````````````````````````````

We assume that you've already valid access credentials (see :ref:`sfaaccess-label`).

.. contents:: Table of Contents


Status of the Testbed
=====================

Check https://flsmonitor.fed4fire.eu to see the status and number of free resources on the Fed4FIRE testbeds, including the FUSECO Playground. You can also check the capabilities of the testbeds also as explained in "Automated Scenario Tests".


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
  
  
  
Automated Scenario Tests
========================

* Automated Testing GUI

The automated scenario tests can be executed using a testing GUI similar to `jFed Probe Tool <http://jfed.iminds.be>`_. Use the `jFed automated testing GUI <http://jfed.iminds.be>`_ (tested with release 1495) to see the capabilities of the testbed. Install the binary and start it via command line::

   java -jar jFed-automated-testing-GUI.jar

* Using the `jFed automated testing GUI <http://jfed.iminds.be>`_

After you start jFed testing GUI, select your certificate and type your password to login.

Select from the target authority dropdown list "fuseco.fokus.fraunhofer.de". This will identify the aggregate manager to be used. The slice manager will be selected automatically based on the certificate you have.

Select from test classes the "be.iminds.ilabt.jfed.lowlevel.api.test.TestAggregateManager3" to test against GENI Aggregate Manager API Version 3.

Now you should configure the test environment. Click on "Test Arguments" to set additional test arguments. Here you should specify at least "fixed_rspec". This is needed first on allocate request and will be used also for further tests. Here is an example how it should look like::

  <rspec type="request" generated="2014-07-11T10:20:39Z" xsi:schemaLocation="http://www.geni.net/resources/rspec/3 http://www.geni.net/resources/rspec/3/request.xsd " xmlns:client="http://www.protogeni.net/resources/rspec/ext/client/1" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.geni.net/resources/rspec/3">
    <node client_id="PC" component_manager_id="urn:publicid:IDN+fuseco.fokus.fraunhofer.de+authority+cm" component_id="urn:publicid:IDN+localhost+node+fOpenStack" exclusive="true">
      <sliver_type name="m1.tiny"><disk_image name="fed4fireNightlyTest"/>
      </sliver_type>
    </node>
  </rspec>

If you want to test accessability using another ssh key pair, you can add these also as extra arguments. To do so choose a file for  "fixed_ssh_public_key_file" and "fixed_ssh_private_key_file" by clicking the button next to these arguments. Afterwards type the password for the ssh private key into the textbox for the argument "fixed_ssh_private_key_password".

Click on "Run Tests" and see the capabilities of the testbed for the automated scenario tests.


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

