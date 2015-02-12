Crash Course Into Python
========================

These IPython notebooks are hosted at https://git.ias.u-psud.fr .

## Summary

These notebooks are meant for you to be able to easily switch to programming in Python. Therefore, you must have some programming skills before starting, ideally in an high-level language like IDL.

**NEW:** you will find on [this page](Useful_links.md) a **list a useful links** towards more specific tutorials on every library used in this session + Git tutorials.

## Requisite / Installation

In order to use this notebook, you will need to install first IPython Notebook

- http://ipython.org/install.html

You can also read [PythonInstall.md](PythonInstall.md) to know how to install and use Python and IPython on your system.

And you will also need several python librairies :

- numpy      : http://docs.scipy.org/doc/numpy/user/install.html
- matplotlib : http://matplotlib.org/1.3.1/users/installing.html
- astropy    : http://docs.astropy.org/en/stable/install.html
- healpy     : https://healpy.readthedocs.org/en/latest/install.html

All those packages can be installed using pip like

```shell
$ pip install --no-deps healpy
```

or using your favorite package application, for e.g. under Debian you can install them with

```shell
$ sudo apt-get install ipython-notebook python-pip python-numpy python-matplotlib python-astropy
```

Make sure to have the latest version (especially astropy), we will try to keep those notebooks updated.


You can now clone the notebooks with git and use them

```shell
$ git clone https://git.ias.u-psud.fr/abeelen/python-notebook.git
$ cd python-notebook
$ ipython notebook
```

In case of an error, you might need to disable the SSL CERT verification, as IAS does not have a trusted SSL certificate

```shell
$ export GIT_SSL_NO_VERIFY=true
```

before launching the `git clone` command.


## Organization

The notebooks are divided into two categories

1. Start
  1. Basic Python
  2. Numpy
  3. Matplotlib
  4. Astropy
  5. Healpy
  6. Optimization
  7. Documenting
  8. Curve Fitting

2. Advanced
  1. Testing
  2. Advanced Python
  3. Classes
  4. Curve Fitting

Be sure to understand and practice all beginner notebooks before going to advanced.

## Authors

Alexandre Beelen, Benjamin Bertincourt, Alexandre Boucaud, Elie Soubrié, Karin Dassas.
