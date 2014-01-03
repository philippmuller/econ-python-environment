.. _eclipse_waf:

Setting up Eclipse to debug your Waf files
=============================================

Associating wscript files with PyDev
______________________________________

PyDev will recognise files with the ``.py`` extension as Python files, but it has no way of knowing that files called "wscript" are also Python scripts. When you double-click on them, they will open in a standard editor window and you will not have syntax highlighting, the ability to set breakpoints, or any of the extra functionality of PyDev to work with these.

In order to change this, go to::
    
    Preferences -> General -> Editors -> File Associations -> Add...

.. image:: associating_wscript_eclipse_1.png
    :width: 12cm

Type ``wscript`` and ``OK``.

.. image:: associating_wscript_eclipse_2.png
    :width: 12cm

Make sure that ``wscript`` is highlighted in the upper panel and select ``Add ...`` from the file associations panel:

.. image:: associating_wscript_eclipse_3.png
    :width: 12cm

From ``Internal Editors``, select ``Python editor`` and click ``OK``.

.. image:: associating_wscript_eclipse_4.png
    :width: 8cm

Done! 


Debugging Waf from Eclipse
_____________________________

PyDev will only let you start the debugger from files having a ``.py`` extension -- but the ``waf`` script typically does not have one. You can either make a copy of it and call it ``waf.py`` or just rename it. You can then start the debugger from ``waf.py`` and set breakpoints in the ``wscript`` files as you like.


.. Eclipse parallel tools: Install debugger
.. Link:
.. http://www.eclipse.org/downloads/download.php?file=/tools/ptp/updates/indigo/ptp-proxy-5.0.0-I201106140904.zip
.. Potentially updated versions (see section "Optional PTP Server Components")
.. http://www.eclipse.org/ptp/downloads.php
.. Instructions:
.. http://wiki.eclipse.org/PTP/release_notes/5.0#Install_optional_PTP_server_components

