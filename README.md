Crash Course Into Python
========================

## Summary

These notebooks are meant for you to be able to easily switch to programming in Python. Therefore, you must have some programming skills before starting, ideally in an high-level language like IDL.

## Requisite / Installation

In order to use this notebook, you will need to install ipython notebook

http://ipython.org/install.html

You will also need several python librairies : 

- numpy      : http://docs.scipy.org/doc/numpy/user/install.html
- matplotlib : http://matplotlib.org/1.3.1/users/installing.html
- astropy    : http://docs.astropy.org/en/stable/install.html
- healpy     : https://healpy.readthedocs.org/en/latest/install.html

All those packages can be installed using pip like
> pip install --no-deps healpy

under Debian you can also use system packages 
> sudo apt-get install ipython-notebook python-pip python-numpy python-matplotlib python-astropy

Make sure to have the latest version (especially astropy), we will try to keep those notebook updated

And then launch the notebook with 

> ipython notebook --pylab inline

## Organization

The notebooks are divided into two categories

1. Start
  1. Basic Python
  2. Numpy
  3. Matplotlib
  4. Astropy
  5. Healpy
  6. Optimization

2. Advance

Be sure to understand and practice all beginner notebooks before going to advance.

## Authors

Alexandre Beelen, Benjamin Bertincourt, Alexandre Boucaud, Karin Dassas.