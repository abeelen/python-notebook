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

### Windows
TBD

### Linux
TBD

### OSX

#### Anaconda

[Main page](https://store.continuum.io/cshop/anaconda/) | [Quick guide (pdf)](https://store.continuum.io/static/img/Anaconda-Quickstart.pdf)

#### Canopy (previously Enthought Python)

[Main page](https://www.enthought.com/products/canopy/)

#### Source

You can get the version of Python you want directly from the [official site](https://www.python.org/downloads/) or using a package manager like MacPorts, Fink or [Homebrew](http://brew.sh/) (_recommended_)

Example using Homebrew
```bash
$ brew install python   # version 2.7.X
$ brew install python3  # version 3.X.X
```

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


## Installing libraries/modules

Python is usually delivered with [pip](https://pip.pypa.io/en/latest/), a library manager.

You can use `pip` to install your libraries (`pip3` for python 3.X) , separating them with a space
```bash
$ pip install scipy numpy matplotlib
```
----
__Tip:__ if you have multiple libraries you need to install, you can list them in a .txt file and have `pip` parse them and install them all at once using the `-r` option, e.g.
```bash
pip install -r requirements.txt
```
----

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
----
__Tip:__ `pip` is a Python module on its own and has to be updated as well, through the command
```bash
$ pip install --upgrade pip
```
----

## PATH and PYTHONPATH

While the PATH is used by the system shell to locate _executables_, the PYTHONPATH is used by Python to locate its _libraries_.

### PATH (for OSX / Linux, Windows should be similar but not covered here)
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

All the libraries installed using `pip` or your package manager should be symlinked to the right place and made usable directly.

For external libraries, installing them with the command `python setup.py install` symlinks them.

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
