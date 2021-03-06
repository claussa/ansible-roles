# Install

These instructions allow you to install all the required Python 3 and Ansible Galaxy dependencies locally (in a Python 3 virtualenv for ansible itself and other Python 3 dependencies, and in a subfolder for the Ansible Galaxy roles).

You need to install Python 3 and pip3 globally on your system.

```
pip3 install virtualenv
```

Create a python3 virtual env in `./env` :

```
virtualenv --python=python3 env
```

Change your current shell environnement variables so that running python or pip will actually use your local installation of Python 3.

```
source env/bin/activate
```

Install the Python 3 dependencies from PyPi:

```
pip install -r requirements.txt
```

Reload the virtual env to get the latest ansible CLI commands

```
source env/bin/activate
```

Install the Ansible dependencies from Ansible Galaxy:

```
ansible-galaxy install -r requirements.yml
```

You can now run the `ansible-playbook` command.
If you close your shell, you need to re-run the `source env/bin/activate` command to re-activate the virtualenv.
