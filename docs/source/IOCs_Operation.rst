TomoScan BEATS IOCs
====================

.. two dots (..) ===> comments
.. .................................................
.. .................................................

Follow the procedures below to run the IOCs:

    .. hyperlink in local page

    * `PCOADWin driver IOC`_
    * `Motor IOC`_
    * `TomoScan Support IOC`_
    * `Writer Support IOC`_
    * `TomoScan IOC`_

.. admonition:: Hint

    It is preferable to open a new tab for each IOC. Also, it is preferable to run each IOC in tmux.

.. .................................................
.. .................................................

PCOADWin driver IOC
--------------------
    1. Login to windows DAQ server.
    2. Run cmd.

    .. admonition:: Recommended

        It is preferable to start Console Emulator: |ConEmu|

         .. |ConEmu| image:: /ConEmu.png
                    :scale: 10%


    3. Go to ``c:\pcoIOC``.
    4. Type this ``bin\windows-x64\ioc.exe iocBoot\ioc\st.cmd``.

    .. admonition:: Very Important!

        Before going to next step, please make sure to run **CentOS 7 VM** on windows DAQ Server.

.. ...............................................
.. ...............................................

Motor IOC
----------
    1. ssh -X to the server **10.1.50.205** using dev.control username.
    2. cd ``/home/dev.control/top/mirrors``.

    .. note::

        Check if the IOC is running by typing: *tmux ls*.
        if not, type this command to run the IOC: ``tmux new -s ShutterIOC``, then: ``/bin/linux-x86_64/ioc iocBoot/ioc/st.cmd``.

    **Some Other Virtual Motors**
    1. ssh -X to the server 10.1.50.12 using root account.
    2. cd ``/opt/top/motor-sim``.

    .. note::

        Check if the IOC is running by typing: *tmux ls*.
        if not, type this command to run the IOC: ``tmux new -s MotorIOC``, then: ``./bin/linux-x86_64/ioc iocBoot/ioc/st.cmd``.

.. .................................................
.. .................................................

TomoScan Support IOC
---------------------
    1. ssh -X to the server 10.1.50.16 using root username.
    2. cd ``/opt/epics7/synApps/support/suppIoc``.

    .. note::

        Check if the IOC is running by typing: *tmux ls*.
        if not, type this command to run the IOC: ``tmux new -s TomoScanSupportIOC``, then: ``softIOC -d suppIoc.db``.

.. .................................................
.. .................................................

Writer Support IOC
-------------------
    1. ssh -X to the server 10.1.50.21 using root username.
    2. cd ``/opt/DCA/BEATS_DAQ_Supp_IOC``.

    .. note::

        Check if the IOC is running by typing: *tmux ls*.
        if not, type this command to run the IOC: ``tmux new -s WriterSupportIOC``, then: ``softIOC -d writerStatus.db``.

.. .................................................
.. .................................................

TomoScan IOC
-------------
    1. Login to tomoscan console (local device 10.1.50.202) using root username. 
    2. cd ``"/opt/epics/synApps/support/tomoscan/iocBoot/iocTomoScan_BEATS_Step"`` for Step scan or ``/opt/epics/synApps/support/tomoscan/iocBoot/iocTomoScan_BEATS_Continuous`` for Continuous scan.

    .. note::

        Check if the IOC is running by typing: *tmux ls*.
        if not, type this command to run the IOC: ``tmux new -s tomoscanIOC``, then: ``./start_IOC``.

    .. warning::

        The selection between Step and Continuous scan depends on **Writer Server** selection.