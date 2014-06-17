FUSECO Playground Resource Description
======================================

Femto Cells
-----------
	
The Base Stations we use are commercial off-the-shelf elements. Usually they support basic functionality.

ip.access nanoBTS (DCS 1800)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Frequency range 1710-1785MHz , 1805-1880MHz , Maximum o/p power +23dBm, +13dBm (8PSK)
supports the ip.access "A-bis over IP Interface"
supports "typical" GSM BTS operations such as
measurement pre-processing
handover
cell broadcast
transmission of system information
transmission and reception of "Full rate" or "Enhanced Full rate" speech traffic
supports full rate and half rate Advanced Multi-Rate speech codec (AMR) on 165 with SR3 and higher software
transmission and reception of circuit switched data;
A5/1, A5/2 or A5/3, or "no encryption" algorithms over the air interface
interworks with the ip.access nanoBSC product
stores non volatile parameters in EEPROM
Supports handover to UMTS cell


ip.access Nano3G E16 (model 239A) UMTS IMT 2100
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Support for 8 or 16 users
Support for 3GPP R99 and HSDPA
Support for HSUPA
250mW transmitter power
Hard handover: inter-frequency, intra-frequency and inter-RAT
IP Backhaul
High stability internal master oscillator
NTP for time/date, OCXO for frequency stability
Configurable to operate with or without IPsec
Full Compliance for 3GPP Local Area Base Station specifications
Total transmit power:

+24dBm (250mw) Bands 1, 2, 4
+13dBm (20mw) Band 5
Receive sensitivity typically -115dBm
Absolute frequency stability of better than +/-100ppb per annum under normal operating conditions
Operational range of 200m for 12.2kbps CS voice calls (assumes an unobstructed path and ITU Pedestrian A propagation conditions)
Uu Encryption and Integrity Protection F8 and F9


ip.access LTE AP (model 254f )  2.6 GHz
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

3GPP Compliance Compliant to 3GPP Rel 8.9.0
Number of RF Carriers Single Carrier
3GPP Band Support Dual Band 1/13, 4/13, 2/5 or 7/13.
Bandwidth 10Mhz
MIMO 2x2 MIMO-Single User Downlink only
RF Average Output Power 2 x 10dBm
Modulation/Coding? 16QAM U/L and D/L
Max Data Rate Throughput 13Mbps
Simultaneous # Active Users 4
Simultaneous # Idle Users 64
Network Interfaces S1 over IP
Electrical Supply 12V @ 5.5A from external power brick


WiFi APs
--------

Support 802.11 a/b/g/n/ac 2,4 GHz and 5 GHz in parallel

HW: Cisco Aironet 3602e


Radio	Signal Attenuation	System
--------------------------------

Frequency range 700MHz – 3GHz; 
Configuration 6x1; 
Attenuation range 1 - 127dB in 1dB steps; 
Switching speed <4 ms

Based on remote commands the attenuation of the signal on all RF inputs can be attenuated in range 1-127dB. 
This allows to simulate users' mobility inside the network range influencing quality of the radio link and allowing to trigger handovers.


Radio	Signal Shield	Box
-----------------------

>80dB shielding; 
USB 2.0 connector; 
Size inside 340 x 240 x 160 mm; 
Antenna Coupler with frequency range 700MHz – 2.7GHz


FUSECO Clients
--------------

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

TBD


OpenIMS Core
------------

TBD

OpenEPC as a Service
--------------------

TBD

FUSECO Cloud Testbed
--------------------

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
