.. _macos_specifics:

MacOS specifics (adjust slightly for Linux)
============================================

.. _macos_terminal:

Opening a Terminal on MacOS
______________________________________

Open the program **Terminal** in the "Utilities" subfolder of your applications folder.

If you have never used the command line before, check `this page <http://www.hacktheday.com/beginners-guide-to-apple-terminal-part-1/>`_ for moving between directories, working with files, etc.. `This lecture <http://software-carpentry.org/4_0/shell/>`_ of the `Software Carpentry course <http://software-carpentry.org/4_0/>`_ goes into more detail. 



.. _path_macos_permanent:

Making the PATH settings permanent on MacOS
_________________________________________________

You will need to add a line to the file ``.bash_profile`` and potentially create the file. This file lives in your home directory and it is hidden from your view by default, to toggle that setting that you can download a neat little `program <http://download.cnet.com/Show-Hidden-Files/3000-2383_4-75415396.html>`_.

**Linux users**: For most distributions, everything here applies to the file ``.bashrc`` instead of ``.bash_profile``.

I will now provide a step-by-step guide of how to create / adjust this file using a tiny editor called ``nano``, if you are familiar with editing text files, just use your editor of choice. 

#. Open a Terminal and type::

        nano ~/.bash_profile

   You will see something like the following:

   .. image:: macos_nano.png
       :width: 12cm

   If ``.bash_profile`` already existed, you will see some text at this point. If so, use the arrow keys to scroll all the way to the bottom of the file. 

#. Paste the following line at the end of the file::

        export PATH="${HOME}/anaconda/envs/py33/bin:${HOME}/anaconda/bin:${PATH}"

   Press ``Return`` and then ``ctrl+o`` (= WriteOut = save) and ``Return`` once more.


#. Now press ``Command+n`` in order to open a new Terminal window and type ``ipython``. You should see something like::

        xxx@xxx-desktop:~/econ$ ipython
            Python 3.3.2 |Anaconda 1.5.1 (x86_64)| (default, Aug  5 2013, 15:07:24) 
            Type "copyright", "credits" or "license" for more information.

            IPython 1.1.0 -- An enhanced Interactive Python.
            ?         -> Introduction and overview of IPython's features.
            %quickref -> Quick reference.
            help      -> Python's own help system.
            object?   -> Details about 'object', use 'object??' for extra details.

   Check the version number -- it should be 3.3, nothing else.

.. note::

    If you have Stata (Matlab, R, ...) installed and intend to use it in your research, you may as well append the path pointing to the respective executable to your path.

    Example for Stata::

        # Stata directory
        PATH="${PATH}:/Applications/Stata/StataMP.app/Contents/MacOS/"
        # Finish
        export PATH

    In the ``path/to/Stata/`` you may need to replace bits and pieces as appropriate for your installation (e.g. you might not have StataMP but StataSE).

    Same for Matlab / R / whatever.


