.. _additional_python_libraries:

Additional Python libraries
=============================

Now we can easily install more libraries. Type::

    conda install -n py33 statsmodels
    pip install -n py33 coverage
    pip install -n py33 sphinxcontrib-bibtex

.. note::

    **Students who only follow the Microeconometrics class are done now and should test their environment using the following steps.**

    Test whether everything installed correctly by typing in a command prompt::

        ipython notebook

    Your default browser should fire up. If you get a ``UnicodeDecodeError``, most likely your computer name contains special characters. Assuming you are on Windows, do the following:

        * Type sysdm.cpl into the start menu search box
        * Change your computer name to pure ASCII characters
        * Restart

    Click on "New notebook" and type::

        import sys
        sys.version

    followed by "Shift + Enter". It should say::

        '3.3.5 |Anaconda ... '

    If it does not, you need to modify your path settings, moving the Python 3.3 environment first (the standard Anaconda install then comes first on your path).

    Then type::

        import statsmodels as sm

    If no error occurred, you are done!


.. raw:: latex

    \clearpage
