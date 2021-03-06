.. DeepLINCS documentation master file, created by
   sphinx-quickstart on Sat Aug  3 09:32:38 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

DeepLINCS: A framework for deep learning with LINCS L1000 Data
==============================================================

DeepLINCS offers a variety of utilities for working with 
`L1000 data <http://www.lincsproject.org/LINCS/tools/workflows/find-the-best-place-to-obtain-the-lincs-l1000-data>`_ 
and training deep learning models. 

The class :class:`Dataset`, built on `pandas dataframes <https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html>`_, 
offers methods to load, sample, filter, subset, and explore these data in memory. 

DeepLINCS also provides a wrapper around around `TensorFlow <https://www.tensorflow.org/beta>`_ 
to efficiently load a :class:`Dataset` and train a variety of deep learning models on the GPU.

You can find the software `on github <https://github.com/manzt/deep_lincs>`_.

Installation
------------

.. code:: bash

     pip install deep-lincs


Downloading the data
--------------------

The data for 1.3 million L1000 profiles are availabe `on GEO <https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE92742>`_.
The script ``load_files.sh`` fetches the ``Level 3`` data along with all metadata available. The largest file is quite big (~50Gb) so please be patient.

.. code:: bash
    
    git clone https://github.com/manzt/deep_lincs.git && cd deep_lincs
    source load_files.sh # download raw data from GEO


Getting started
---------------

Navigate to the `example notebooks <https://github.com/manzt/deep_lincs/tree/master/notebooks>`_ and try building a model!

.. code:: bash

    cd notebooks
    jupyter lab # easiest for plotting with altair
    

High-level API reference
------------------------
.. toctree::
    :maxdepth: 1

    dataset

.. toctree::
    :maxdepth: 1

    settings
    
.. toctree::
    :maxdepth: 2

    models


