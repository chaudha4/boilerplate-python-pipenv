pipenv
======

Project was initialized with [pipenv](https://pipenv.pypa.io/en/latest/)

## Steps

### Specifying Versions of Python
To create a new virtualenv, using a specific version of Python you have installed (and on your PATH), use the --python VERSION flag
```
pipenv --python 3
```
You can also use `pipenv --three` to setup a python 3 virtual env.

## Install new packages
1. Install a package
```
pipenv install requests
```
### Specifying Versions of a Package
You can specify versions of a package using the Semantic Versioning scheme (i.e. major.minor.micro).
For example, to install requests you can use:
```
pipenv install requests~=1.2
```
Pipenv will install version 1.2 and any minor update, but not 2.0.
This will update your Pipfile to reflect this requirement, automatically.

## Install dev only packages (optional)
1. Install a dev only dependency. This will also update the `PipFile`.
```
pipenv install pytest --dev
```

## Importing from requirements.txt (Optional)
If you only have a requirements.txt file available when running pipenv install, pipenv will automatically import the contents of this file and create a Pipfile for you
```
pipenv install -r path/to/requirements.txt
```
## Uninstall Packages
`pipenv uninstall` supports all of the parameters in pipenv install, as well as two additional options, --all and --all-dev.
* --all — This parameter will purge all files from the virtual environment, but leave the Pipfile untouched.
* --all-dev — This parameter will remove all of the development packages from the virtual environment, and remove them from the Pipfile.

## Generating a `Pipfile.lock`
`pipenv lock` is used to create a Pipfile.lock, which declares all dependencies (and sub-dependencies) of your project, their latest available versions, and the current hashes for the downloaded files. This ensures repeatable, and most importantly deterministic, builds.

## Generating a `requirements.txt` file
Sometime you may need a `requirements.txt` file for your deployment. You can generate it using
```
pipenv lock -r
```
This will include all hashes, however (which is great!). To get a requirements.txt without hashes, use 
```
pipenv run pip freeze.
```



##  Other Useful Commands

- Locate the project
```
$ pipenv --where
/home/chaudha4/Projects/pyprojects/hello-world
```
- Locate the Python interpreter
```
$ pipenv --py
/home/chaudha4/.local/share/virtualenvs/hello-world-wrhdU98Z/bin/python
```
- Locate the virtualenv
```
$ pipenv --venv
/home/chaudha4/.local/share/virtualenvs/hello-world-wrhdU98Z
$ 
```
- See the dependency graph
```
$ pipenv graph
appdirs==1.4.3
CacheControl==0.12.6
certifi==2019.11.28
urllib3==1.25.8
webencodings==0.5.1
```
