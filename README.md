# iiwa_setup
iiwa real world setup

## Installation

This repo uses Poetry for dependency management. To setup this project, first install
[Poetry](https://python-poetry.org/docs/#installation) and, make sure to have Python3.10
installed on your system.

Then, configure poetry to setup a virtual environment that uses Python 3.10:
```
poetry env use python3.10
```

Next, install all the required dependencies to the virtual environment with the
following command:
```
poetry install -vvv
```
(the `-vvv` flag adds verbose output).

For local Drake and manipulation installations, insert the following at the end of the
`.venv/bin/activate` and `.venv/bin/activate.nu` files, modifying the paths and python
version as required:
```bash
export PYTHONPATH=""
export PYTHONPATH=~/drake-build/install/lib/python3.10/site-packages:${PYTHONPATH}
export PYTHONPATH=~/manipulation:${PYTHONPATH}
```

Activate the environment:
```
poetry shell
```