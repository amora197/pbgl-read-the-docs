.. sphinx-tutorial documentation master file, created by
   sphinx-quickstart on Fri Dec  4 11:08:12 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

ReadtheDocs Documentation
=========================

.. toctree::
   :maxdepth: 2

Background
^^^^^^^^^^

This tutorial describes a step-by-step tutorial to create a ReadtheDocs website and PDF file of an already created GitHub repository, using `sphinx <https://www.sphinx-doc.org/en/master/>`_, `LaTex <https://www.latex-project.org/>`_, `conda <https://docs.conda.io/en/latest/>`_, and `git <https://git-scm.com/>`_.

.. note::
   
   This is run using Ubuntu 18.04 Bionic Beaver. For different Ubuntu distributions, download and install the appropriate software/packages.

   Code ran on Linux terminal is preceded by ``$``.

Installing conda and Setting Up bioconda Channels
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

It is recommended to install miniconda3 and create a conda environment to install all necessary packages and dependencies without affecting the system. Miniconda is a free minimal installer for conda. It is a small, bootstrap version of Anaconda that includes only conda, Python, the packages they depend on, and a small number of other useful packages, including pip, zlib and a few others. Use the conda install command to install 720+ additional conda packages from the Anaconda repository.

Open a new terminal **(Ctrl + Alt + T)** and make sure that the system is up-to-date,

:: 

   $ sudo apt-get update

Download the latest package from the '`Miniconda Webpage <https://docs.conda.io/en/latest/miniconda.html>`_ and install it with,

::

   $ curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
   $ sh Miniconda3-latest-Linux-x86_64.sh

It may be possible that Python 2.7 was installed with miniconda3. In order to use a newer version of Python, install the preferred Python version and update conda to resolve any dependency failures,

::

   $ conda install -c anaconda python=3.7

Setup the appropriate bioconda channels. Make sure to run the following commands exactly in this order,

::

   $ conda config --add channels defaults
   $ conda config --add channels bioconda
   $ conda config --add channels conda-forge

Bioconda is now enabled, so you can install any packages and versions available on the bioconda channel.

Creating a conda environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Create a new conda environment with:

::

   $ conda create --name <environment-name>

Substitute ``<environment-name>`` with the preferred name you want. As an example, 

::

   $ conda create --name sphinx-tutorial

Once the newly created environment has been installed, activate it to make the neccesary installations. Activate the conda environment with,

::

   $ conda activate sphinx-tutorial

If more than one conda environment exists, the previously created conda environments can be listed in the terminal by running, 

::

   $ conda env list

Installing sphinx, LaTex, and git
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Install git, sphinx and LaTex using by conda with,

::

   $ conda install git
   $ conda install sphinx
   $ conda install sphinx_rtd_theme
 
LaTex cannot be installed with conda, so the installation is done with,

   $ sudo apt-get install texlive-latex-extra

Cloning the GitHub Repository to Local Machine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^











.. figure:: ../images/function_02_output.jpeg
   :width: 600px
   :align: center
   :figclass: align-center

   "GTPlotting_Chromosome" output. (click to expand)




