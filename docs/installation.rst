.. _install:

************
Installation
************

Dependencies
============

Python 2.7 and 3.4+ are supported.

``pyregion`` has the following required dependencies:

* `Astropy <http://www.astropy.org/>`__ version 1.0 or later (which requires Numpy)
* ``pyparsing`` version 2.0 or later for parsing the DS9 region files
    * `Homepage <http://pyparsing.wikispaces.com/>`__
    * `PyPI page <https://pypi.python.org/pypi/pyparsing>`__

``pyregion`` has the following optional dependencies for plotting:

* `matplotlib <http://matplotlib.org/>`__
* `wcsaxes <https://github.com/astrofrog/wcsaxes>`__

To work with the development version, you'll need Cython and a C compiler,
because the code to generate masks from regions is written in Cython.

Stable version
==============

Installing the latest stable version is possible either using pip or conda.

Using pip
---------

To install pyregion with `pip <http://www.pip-installer.org/en/latest/>`_
from `PyPI <https://pypi.python.org/pypi/pyregion>`_
simply run::

    pip install --no-deps pyregion

.. note::

    The ``--no-deps`` flag is optional, but highly recommended if you already
    have Numpy installed, since otherwise pip will sometimes try to "help" you
    by upgrading your Numpy installation, which may not always be desired.

Using conda
-----------

To install regions with `Anaconda <https://www.continuum.io/downloads>`_
from the `astropy channel on anaconda.org <https://anaconda.org/astropy/pyregion>`__
simply run::

    conda install -c astropy pyregion


Testing installation
--------------------

To check if your install is OK, run the tests:

.. code-block:: bash

    python -c 'import pyregion; pyregion.test()'

Development version
===================

Install the latest development version from https://github.com/astropy/pyregion :

.. code-block:: bash

    git clone https://github.com/astropy/pyregion
    cd pyregion
    python setup.py install
    python setup.py test
    python setup.py build_docs
