# Getting a working Python environment

## Installation

Python is installed by default on most machines.

The path to the default Python executable can be found by running the command-line
`which python` ; e.g.
```bash
$ which python
/usr/local/bin/python
```
and the version of the program can be retrieved using `python --version`.

The default version is usually the system one and is not easily tunable.
For scientific purposes it is better to start with a clean install, or use dedicated versions (Anaconda, Canopy) bundled with all the major scientific and plotting libraries.

### OSX
OSX comes with a default python environement. However, on OSX, it is often better to install a dedicated scientific python environement.

They are different ways to install a python environement on OSX, using package manager like MacPorts, Fink or [Homebrew](http://brew.sh/) (_recommended_)

* **Homebrew**

    Example using Homebrew

```bash
$ brew install python   # version 2.7.X
$ brew install python3  # version 3.4.X
```

the dedicated scientific environments:

* **Anaconda**

    [Main page](https://store.continuum.io/cshop/anaconda/) | [Quick guide (pdf)](https://store.continuum.io/static/img/Anaconda-Quickstart.pdf)


* **Canopy** (previously Enthought Python)


    [Canopy](https://www.enthought.com/products/canopy/) provide a complete python environement and way to install packages.

or from **source**:

* official source

You can get the version of Python you want directly from the [official site](https://www.python.org/downloads/).

### Linux

Most distributions provide a package to install python. Please refer to your Operating System documentation. Some also provide way to deal with multiple python versions installed at the same time.

You could also use a dedicated scientific python environment provided by e.g. Canopy or Anaconda (see OSX).

### Windows
TBD (or not)

---
## Running a Python environment

Enter the program typing `python` in a terminal:
```
$ python
Python 2.7.8 (default, Oct 16 2014, 05:18:45)
[GCC 4.2.1 Compatible Apple LLVM 6.0 (clang-600.0.51)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
and type in the prompt `quit()`, `exit()` or `Ctrl-D` on your keyboard to exit the program.

---

## Libraries & Modules

Python has many libraries from numerical calculation to plotting or image processing.

### Installation

Your Operating System usually provide package with the most common python libraries and module. Moreover Python is usually delivered with [pip](https://pip.pypa.io/en/latest/), a library manager.

If you use Anaconda or Canopy Python, they are already shipped with most of the scientific libraries pre-installed. In case the library of your choosing is not installed, please refer to the documentation of these environments for their installation and maintenance.

However for a custom installation of Python you can use `pip` to install your libraries (`pip3` for Python 3.X) , separating them with a space
```bash
$ pip install scipy numpy matplotlib
```

__Tip:__ if you have multiple libraries you need to install, you can list them in a .txt file and have `pip` parse them and install them all at once using the `-r` option, e.g.
```bash
pip install -r requirements.txt
```


### Library maintenance

Python libraries are __often__ upgraded.

If you want to know which of your libraries are outdated
```bash
$ pip list --outdated
```
and then upgrade them
```bash
$ pip install --upgrade scipy numpy matplotlib
```

__Tip:__ `pip` is a Python module on its own and has to be updated as well, through the command
```bash
$ pip install --upgrade pip
```

---
## IPython / IPython notebook

In order to use Python in an interactive way, IPython must be installed. You can find informations about IPython and its installation on their [website](http://ipython.org/install.html).

IPython provides you with autocompletion, inverse/history search, help in terminal as well as some magic functions.

Once the libraries `numpy` and `matplotlib` have been installed on your computer, running IPython with the `--pylab` option
```bash
$ ipython --pylab
```
loads all the methods of these two libraries. There is thus no need to import them to create arrays, quickly plot data, etc.

### Notebook

An other great feature of IPython is the [notebook](http://ipython.org/notebook.html) (similar to those of *Mathematica*), a web-based interactive environment where you can combine text, code execution and plots in a single document.

Running in a terminal the command
```bash
ipython notebook
```
creates a python kernel in the background and opens in a browser a local interface. From there you can interact with notebooks, which are saved as `.ipynb` files.

---
## PATH and PYTHONPATH

While the PATH is used by the system shell to locate _executables_, the PYTHONPATH is used by Python to locate its _libraries_.

### PATH (for *nix)

The Python version used by the system is the one that appears __first__ in your `PATH` variable.
Thus make sure you prepend the path to your (new) python executable to your `.bashrc` as

```bash
PATH=/path/to/your/python:${PATH}
```

Likewise, if you have a python program, say ___program.py___ (that has been made executable using `chmod +x program.py`) and located in /path/to/program, you need to type the full path in your terminal, e.g.

```bash
$ /path/to/program/program.py
```

in order to run it.
Now if you add /path/to/program to the PATH variable in your `.bashrc`

```bash
PATH=${PATH}:/path/to/program
```

___program.py___ will be recognised by the system as an executable (with add auto-completion) and you'll just have to type

```bash
$ program.py
```

wherever you are.

### PYTHONPATH

All the libraries installed using `pip` or your package manager should be installed in standard places, where Python know where to look. For external libraries, installing them with the command `python setup.py install` will copy them at the right place, usualy `/usr/local/lib/`.

However, for your own libraries (even simple scripts), their path needs to be appended to the `PYTHONPATH` variable in the `.bashrc` file

```bash
PYTHONPATH=${PYTHONPATH}:/path/to/your/libraries
```

so that you can open a Python environment and import them
```
$ python
Python 2.7.8 (default, Oct 16 2014, 05:18:45)
[GCC 4.2.1 Compatible Apple LLVM 6.0 (clang-600.0.51)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import mylib
>>>
```
