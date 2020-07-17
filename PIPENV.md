pipenv
======

Project was initialized with [pipenv](https://pipenv.pypa.io/en/latest/)

## Steps

1. Created the env using `pipenv --three`
1. Install all dependencies for a project (including dev) using `pipenv install --dev`

## Install new packages

1. Install a dev dependency. This will also update the `PipFile`.
```
pipenv install pytest --dev
```

##  Useful Commands

1. Locate the project
```
$ pipenv --where
/home/chaudha4/Projects/pyprojects/hello-world
```
2. Locate the Python interpreter
```
$ pipenv --py
/home/chaudha4/.local/share/virtualenvs/hello-world-wrhdU98Z/bin/python
```
3. Locate the virtualenv
```
$ pipenv --venv
/home/chaudha4/.local/share/virtualenvs/hello-world-wrhdU98Z
$ 
```