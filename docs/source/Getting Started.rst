Getting Started
===============

Set-Up
++++++

The MATS package was developed and tested using the `Anaconda <https://www.anaconda.com/>`_ python environment. Example scripts have typically been written and run using  `jupyter notebooks <https://jupyter.org/>`_ (run in jupyter lab), as this allows for code to be run in segments and for iteration on certain code segments.  Any python package distribution should work with the code as long as the dependent packages are installed.


Main Packages
+++++++++++++

* `MATS <https://github.com/usnistgov/MATS>`_

* `HITRAN Application Programming Interface (HAPI) <https://hitran.org/hapi/>`_   The v1.1.1.0 was tested and is available in the MATS repository.  


Dependent Packages
++++++++++++++++++
MATS is not written as a basic package, meaning that there are several dependent packages that need to be installed. 

If a desired package is not installed then the following command will install it.  Many python package distributions have integrated package managers and required packages can also be installed through that mechanism.

.. code-block:: python

	pip install package_name

There is commonly a delay in the most recent package releases available in python package distribution package managers compared to that available through pip install.  The following command line script will update to the newest release if a package is already installed.  This should only be necessary if there is an error when running MATS with the currently installed version. 

.. code-block:: python

	python -m pip install --upgrade package_name --user

Below are a list of the packages used in MATS. 

* `numpy <https://www.numpy.org/>`_ - python's fundamental scientific computing package
* `pandas <https://pandas.pydata.org/>`_ - python data structure package 
* os, sys - system variables
* `lmfit <https://lmfit.github.io/lmfit-py/fitting.html>`_ - non-linear least-squares minimization and curve-fitting for python
* `matplotlib <https://matplotlib.org/>`_ - python plotting 
* `seaborn <https://seaborn.pydata.org/>`_ - pretty plotting
* `scipy.fftpack <https://docs.scipy.org/doc/scipy/reference/fftpack.html>`_ - provides fft functionality
* `jupyter lab <https://jupyterlab.readthedocs.io/en/stable/>`_ - web-based user interface for Project Jupyter


Install
+++++++
Taken from the INSTALL.md file

Basic `MATS` installation instructions.  Note that development is alpha.  In the future, full pypi/conda installs will be made available.

**Create a conda environment with MATS dependencies**

Download the [environment](environment.yml) file.  Note that without setting the environment name below,
by default an evironment `MATS-env` will be created.

.. code-block:: python

	conda env create -n {optional-name-of-environment} -f environment.yml


Alternatively, we provide a conda metapackage `mats-dependencies`, which includes all dependencies for `MATS`` (excluding python).
This can be installed using

.. code-block:: python

	conda install -n {optional-name-of-environment} -c wpk-nist mats-dependencies


**From source**

After cloning the repo, you can do the following.

.. code-block:: python

	pip install .


To install an editable version, use option `-e`.  To exclude dependencies, use option `--no-deps`

**With pip from github**

This requires git also be installed.  Downside is that the whole repo (including all examples) are clones.

.. code-block:: python

	pip install git+https://github.com/wpk-nist-gov/MATS.git@feature/master-reformat


**With pip from github using wheel**
Note, this is experimental.  Do the following


.. code-block:: python

	pip install https://raw.githubusercontent.com/wpk-nist-gov/MATS/feature/master-reformat/wheel/MATS-3-py3-none-any.whl


(Note that the actual version will not be 3)

Alternatively, download the wheel and run

.. code-block:: python

	pip install path-to-wheel.whl





