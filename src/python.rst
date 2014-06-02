.. _python:

Anaconda Python Distribution
==============================

Anaconda is a pre-packaged Python distribution for scientific users. [#]_ 

Direct your browser to http://repo.continuum.io/anaconda3/; download the version for your machine. Then follow the steps described for your machine here: http://docs.continuum.io/anaconda/install.html. You do not need to worry about setting the paths yet.

Be sure to select the link above -- the default Anaconda has Python 2.7, we want Python 3.4.

.. rubric:: Footnotes

.. [#] Python itself installs easily on all systems. It is not geared towards a specific userbase and the scientific tools need to be installed---as libraries---on top of it. This is the tricky part because most of these tools are **wrappers** around fast, battle-tested Fortran or C libraries which you won't have on your machine. So the machine-readable code has to be compiled (=generated) on a machine where these libraries are available; luckily the ContinuumIO team has done that already -- thanks!!! This was a pain in the \*\*\* in previous runs of the course.

