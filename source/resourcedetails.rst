.. _resourcedetails-label:

```````````````````````````````
FUSECO Playground Resource Description
```````````````````````````````

.. contents:: Table of Contents

Femto Cells
===========
	
The Base Stations we use are commercial off-the-shelf elements. Usually they support basic functionality.

ip.access nanoBTS (DCS 1800)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Each nanoBTS is a single TRX which can support up to 14 simultaneous voice calls using dynamic AMR with half-rate. 
For high traffic locations, where even greater capacity is needed, up to 4 nanoBTS can used to create a 2, 3 or 4 TRX cell.
The nanoBTS picocell offers:

* Controllable output power up to 23dBm giving an indoor range up to 200m

* Simple deployment with a single Ethernet connection for power, traffic and signalling

* GPRS and EDGE data essential Blackberry® and enterprise applications

* Models for the 850, 900, 1800 and 1900MHz bands

* Network Listen™ to optimize handover configuration

For futher details see `ip.access <http://www.ipaccess.com/en/public-access>`_

ip.access Nano3G E16 (model 239A) UMTS IMT 2100
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The full +24 dBm (250mW) output power gives the E-class picocells the range to cover medium and large office buildings, 
and for the largest deployments the E-class can connect directly into an active DAS system. 
The flexibility is further enhanced by the high precision oscillator, giving fast start up in areas where no macro network can penetrate.

Features:

* Up to 16 simultaneous active users - (each with concurrent voice and high-speed data sessions) 

* +24 dBm (250mW) output power

* Available for Bands 1, 2/5 and 4.

For futher details see `ip.access <http://www.ipaccess.com/en/public-access>`_


ip.access LTE AP (model 254f )  2.6 GHz
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For futher details see `ip.access <http://www.ipaccess.com/en/public-access>`_

WiFi APs
--------

Support 802.11 a/b/g/n/ac 2,4 GHz and 5 GHz in parallel

HW: Cisco Aironet 3602e


Radio	Signal Attenuation	System
==================================

Frequency range 700MHz – 3GHz; 
Configuration 6x1; 
Attenuation range 1 - 127dB in 1dB steps; 
Switching speed <4 ms

Based on remote commands the attenuation of the signal on all RF inputs can be attenuated in range 1-127dB. 
This allows to simulate users' mobility inside the network range influencing quality of the radio link and allowing to trigger handovers.


Radio	Signal Shield	Box
===========================

>80dB shielding; 
USB 2.0 connector; 
Size inside 340 x 240 x 160 mm; 
Antenna Coupler with frequency range 700MHz – 2.7GHz


FUSECO Clients
==============

Supporting multiple operating systems as well as connectivity to different radio access technologies.

HW: LENOVO ThinkCentre M93 Tiny: Intel Core i5-4570T (2.90 GHz, 4 MB Cache), 1x4 GB PC3-12800 DDR3, 500 GB -7200, Grafik Intel 4600

OpenIMS Client
^^^^^^^^^^^^^^^

`myMONSTER <http://www.monster-the-client.org/index.html>`_ (Multimedia Open InterNet Services and Telecommunication EnviRonment) is an extendible plug-and-play framework developed by Fraunhofer FOKUS. 
This toolkit enables the creation of rich terminal applications compliant to NGN and WEB standards.

myMONSTER provides two toolkits for telecommunication service on the mobile and fixed platform. 
For development on mobile devices, we offer the myMONSTER Rich Communication Suite (myMONSTER RCS) and for desktop/laptops/fixed platforms we offer the myMONSTER Telco Communication Suite (myMONSTER TCS).

OpenEPC Client
^^^^^^^^^^^^^^^

Ability to run and operate the Mobility Manager which: 

* handles the attachments/detachments/handovers for the Client machine.

* measures the signal strengths for 2G,3G,4G,WiFi connections in case physical equipments are used 

* able to communicate on S14 interface with the OpenEPC ANDSF entity

The user is able to reconfigure the Mobility Manager: 

* configure the list of access networks that the user wants to work with (select from the available ones provided by OpenEPC) 

* configure the signal thresholds which determine if a handover is performed or not when an ANDSF policy has to be analyzed 

* whether or not the ANDSF policy gets executed (enabling/disabling network control over the handovers) The user is able to use and configure MONSTER client.


OpenIMS Core
============

The `Open IMS Core <http://openimscore.sourceforge.net/>`_ is an Open Source implementation of IMS Call Session Control Functions (CSCFs) and a lightweight Home Subscriber Server (HSS), 
which together form the core elements of all IMS/NGN architectures as specified today within 3GPP, 3GPP2, ETSI TISPAN and the PacketCable intiative. 
The four components are all based upon Open Source software(e.g. the SIP Express Router (SER) or MySQL).

OpenEPC as a Service
====================

The FUSECO Playground offers access to an OpenEPC Rel. 5 setup as a Service. 

`OpenEPC <http://www.openepc.net/index.html>`_ is a prototype implementation of the 3GPP Evolved Packet Core (EPC). It enables academia and industry researchers and engineers around the world to obtain a practical look and feel of the capabilities of the Evolved Packet Core. 
OpenEPC Rel. 5, the current version available, includes all the components of the 3GPP architecture including the interfaces with various access technologies and service platforms.

FUSECO Cloud Testbed
====================

Is a cloud testbed based on OpenStack.

* Compute ressource
	* DELL PE M620 blades
	* Each blade (PE M620) is equipped with two 6 core CPUs (2,5GHz) and 128GB RAM
	
* Storage
	* NetApp Metro Cluster
	* Capacity: 10TB fully redundant
	
* Network equipment
	* Cisco router
	* Cisco swiches 
	* HP 3800 OpenFlow capable
