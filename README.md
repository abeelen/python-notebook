Crash Course Into Python
========================


These ipython notebooks are hosted at https://git.ias.u-psud.fr . If needed, you can find a git tutorial http://githowto.com .

## Summary

These notebooks are meant for you to be able to easily switch to programming in Python. Therefore, you must have some programming skills before starting, ideally in an high-level language like IDL.

## Requisite / Installation

In order to use this notebook, you will need to install first ipython notebook

- http://ipython.org/install.html

And you will also need several python librairies : 

- numpy      : http://docs.scipy.org/doc/numpy/user/install.html
- matplotlib : http://matplotlib.org/1.3.1/users/installing.html
- astropy    : http://docs.astropy.org/en/stable/install.html
- healpy     : https://healpy.readthedocs.org/en/latest/install.html

All those packages can be installed using pip like
> pip install --no-deps healpy

or using your favorite package application, for e.g. under Debian you can install them with 

> sudo apt-get install ipython-notebook python-pip python-numpy python-matplotlib python-astropy

Make sure to have the latest version (especially astropy), we will try to keep those notebook updated


You can now clone the notebook with git and use them

> git clone https://git.ias.u-psud.fr/abeelen/python-notebook.git

> cd python-notebook

> ipython notebook


## Organization

The notebooks are divided into two categories

1. Start
  1. Basic Python
  2. Numpy
  3. Matplotlib
  4. Astropy
  5. Healpy
  6. Optimization

2. Advanced
  1. Testing
  2. Advanced Python
  3. Classes
  4. Curve Fitting

Be sure to understand and practice all beginner notebooks before going to advanced.

## Authors

Alexandre Beelen, Benjamin Bertincourt, Alexandre Boucaud, Elie Soubrié, Karin Dassas.