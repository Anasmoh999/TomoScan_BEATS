DAQ Servers
============

The following Servers must be running:

    * `Writer Server`_
    * `Python Server`_


Writer Server
--------------
    1. ssh -X to the server 10.1.50.21 using root username.
    2. cd ``/opt/DCA/SW/BEATSH5Writer``.
    3. activate python3 environment by typing: p3
    4. run this command for writing data received from: tomoscan_step ``python runAsServer.py --scanMode Step``. And this one for tomoscan_continous: ``python runAsServer.py --scanMode Continuous``.


Python Server
--------------
    1. cd ``/opt/epics/synApps/support/tomoscan/iocBoot/iocTomoScan_BEATS_Step`` for Step scan or ``/opt/epics/synApps/support/tomoscan/iocBoot/iocTomoScan_BEATS_Continuous`` for Continuous scan.
    2. Type: ``./start_python``.

    .. warning::

        The selection between Step and Continuous scan depends on **Writer Server** selection.
