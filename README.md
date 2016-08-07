# PyCon Canada 2016 Website

The source code for [PyCon Canada's 2016 conference website](https://2016.pycon.ca/).

## Development Environment Setup

You will need the following:

* Python 2.7
* pip
* virtualenvwrapper
* [git-lfs](https://git-lfs.github.com/)

Start by cloning the repository:

```
$ git clone git@github.com:pyconca/2016-web.git
$ cd ~/2016-web
```

Create a python virtual environment:

```
~/2016-web $ mkvirtualenv pycon_web
(pycon_web) ~/2016-web $
```

The `(pycon_web)` prefix indicates that a virtual environment called "pycon_web" is being used. Next, check that you have the correct version of Python:

```
(pycon_web) ~/2016-web $ python --version
Python 2.7.12
(pycon_web) ~/2016-web $ pip --version
pip 8.0.2 from /Users/.../site-packages (python 2.7)
```

Install the project requirements:

```
(pycon_web) ~/2016-web $ pip install --upgrade -r requirements.txt
```

Run the project:

```
(pycon_web) ~/2016-web $ python manage.py runserver
```

## Deployment

```
fab <environment> deploy
```

Environments:

* `stag`
* `prod`
