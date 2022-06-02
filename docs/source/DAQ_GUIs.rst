DAQ GUIs
=========

The following GUIs must be running:

    * `MEDM`_
    * `ImageJ`_

MEDM
-----
    1. cd ``/opt/epics/synApps/support/tomoscan/iocBoot/iocTomoScan_BEATS_Step`` for Step scan or ``/opt/epics/synApps/support/tomoscan/iocBoot/iocTomoScan_BEATS_Continuous`` for Continuous scan.
    2. Type: ``./start_medm``.

    .. warning::

        The selection between Step and Continuous scan depends on **Writer Server** selection.

ImageJ
-------
    1. From Desktop, double click on this icon: |ImageJ|

    .. |ImageJ| image:: /ImageJ.jpg
                :scale: 30%

    2. or from terminal: cd ``/opt/SW/ImageJ/ImageJ``.