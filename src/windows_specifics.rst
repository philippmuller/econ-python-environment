.. _windows_specifics:

*****************
Windows specifics
*****************

.. _win_shell:

Opening a shell on Windows
==========================

#. On **Windows XP**: Click on `Start`, select `run`, type ``cmd``. 
#. On later versions: Click on `Start`, type ``cmd`` in the search field.

   There is an even simpler way that saves you from changing to the right directory: In the Windows Explorer, right-click on the folder you want to go to (you must be in the right panel if you have the split-screen folder view) while holding down the shift key. You'll see an extra context-sensitive menu item there: Open Command Prompt here. Just click on this menu and a command window will open with the current working directory set to the folder's actual location.

If you have never used the command line before, check `this page <http://www.bleepingcomputer.com/tutorials/tutorial76.html>`_ for moving between directories, working with files, etc.


.. _win_path_permanent:

Making the PATH settings permanent on Windows
=============================================

You will need local administration rights for this again.

* Right-click on Computer. Then go to "Properties" and select the tab "Advanced System settings". Choose "Environment Variables" and select "Path" from the list of system variables.
* Choose "Edit" and **prepend**:: 
    
    C:\Anaconda\envs\py33\;C:\Anaconda\envs\py33\Scripts;

  to the variable value -- make sure the rest remains as it is.
* Click on ``OK`` as often as needed.
* Test this by opening a new command prompt in a directory that is not ``C:\anaconda`` and type ``ipython``. You should see something like::

    Python 3.3.2 |Anaconda 1.5.1 (x86_64)| (default, Aug  5 2013, 15:07:24) [MSC v.1500 32 bit (Intel)]
    Type "copyright", "credits" or "license" for more information.

    IPython 1.1.0 -- An enhanced Interactive Python.
    ?         -> Introduction and overview of IPython's features.
    %quickref -> Quick reference.
    help      -> Python's own help system.
    object?   -> Details about 'object', use 'object??' for extra details.

If IPython launches, it worked -- make sure to check the version number, should be 3.3 and not 2.7.


.. _win_path_additional_programs:

Adding additional programs to your path
=======================================

If you plan on using the project template with programs other than Python (Stata, Matlab, R, ...), you will need to add the respective executables to your path as well. Otherwise Waf will not be able to find these programs.

You will need to follow the same steps as before. Example for Stata: Append ``;C:\Path\to\Stata.exe`` to the path in the same fashion now (e.g. if your Stata executable is ``C:\Programme\Stata13\WSESTATA.EXE``, you should add ``;C:\Programme\Stata13`` to your path). Similarly for Matlab / R / etc..

