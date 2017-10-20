PyEER
=====

**PyEER** is a python package with utilities to calculate Equal Error Values, operation points
an to plot the associated curves.

Installing
----------

.. code:: sh

    pip install pyeer

Input file formats
------------------
Histogram format:
1. Only integer scores are supported
2. Impostor file format: Each line contains the number of score equals to the index of the line in the file
(starting from zero). For example, given a file:

123
12
212
321
...
...
...

This means that there are 123 score equals to 0, 12 score equals to 1, 212 score equals to 2, 321 score equals to 3 and so on.

3. Use this format for very large experiments.

Usage
-----

entry point: plot_roc_curves.py

EXAMPLES:

To print the script help

.. code:: sh
    python plot_roc_curves.py -h

One experiment (Non-histogram format):

.. code:: sh
    python plot_roc_curves.py -p "example_files/non_hist/" -i "exp1_false" -g "exp1_true" -e "exp1"

More than one experiment (Non-histogram format):

.. code:: sh
    python plot_roc_curves.py -p "example_files/non_hist/" -i "exp1_false,exp2_false" -g "exp1_true,exp2_true" -e "exp1,exp2"

One experiment (Histogram format):

.. code:: sh
    python plot_roc_curves.py -p "example_files/hist/" -i "exp1_false" -g "exp1_true" -e "exp1" -ht

Contribution Guidelines
-----------------------

Do you find **PyEER** useful? You can collaborate with us:

`Link Gitlab <https://gitlab.com/manuelaguadomtz/pyeer>`_