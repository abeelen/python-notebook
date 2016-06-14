Crash Course Into Python
========================

These IPython notebooks are hosted at https://git.ias.u-psud.fr .

These notebooks are meant for you to be able to easily switch to programming in Python. Therefore, you must have some programming skills before starting, ideally in an high-level language like IDL.

***New*** : All the documentation have been moved to the [wiki](https://git.ias.u-psud.fr/abeelen/python-notebook/wikis/home)

## Notebooks

You can clone these notebooks by using

```shell
$ git clone https://git.ias.u-psud.fr/abeelen/python-notebook.git
$ cd python-notebook
$ ipython notebook
```

In case of an error, you might need to disable the SSL CERT verification, ~~as IAS does not have a trusted SSL certificate~~

```shell
$ export GIT_SSL_NO_VERIFY=true
```

before launching the `git clone` command, and then once the cloning is done
```shell
$ git config http.sslVerify false
```

## Wiki

The wiki pages are accessible with

```shell
$ git clone https://git.ias.u-psud.fr/abeelen/python-notebook.wiki.git
```