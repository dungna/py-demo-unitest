## Overview

This Flask application contains the basic user management functionality (register, login, logout) to demonstrate how to test a Flask project using [pytest](https://docs.pytest.org/en/stable/).

For details on how to test a Flask app using pytest, check out my blog post on [TestDriven.io](https://testdriven.io/):

* [https://testdriven.io/blog/flask-pytest/](https://testdriven.io/blog/flask-pytest/)

![Testing Flask Applications with Pytest](project/static/img/flask_pytest_social.png?raw=true "Testing Flask Applications with Pytest")

## Motivation

After reading [Python Testing with pytest](https://pragprog.com/titles/bopytest/python-testing-with-pytest/) by Brian Okken, I was convinced that I should learn about pytest and then figure out how to use it to test Flask applications.

## How to Run

In the top-level directory:

```sh
$ export FLASK_APP=app.py
$ export FLASK_ENV=development
$ flask run
```

## Installation Instructions

Pull down the source code from this GitLab repository:

```sh
$ git clone git@gitlab.com:patkennedy79/flask_user_management_example.git```
```

Create a new virtual environment:

```sh
$ cd flask_user_management_example
$ python3 -m venv venv
```

Activate the virtual environment:

```sh
$ source venv/bin/activate
```

Install the python packages in requirements.txt:

```sh
(venv) $ pip install -r requirements.txt
```

Set the file that contains the Flask application and specify that the development environment should be used:

```sh
(venv) $ export FLASK_APP=app.py
(venv) $ export FLASK_ENV=development
```

Run development server to serve the Flask application:

```sh
(venv) $ flask run
```

Navigate to 'http://localhost:5000' to view the website!

## Key Python Modules Used

* Flask: micro-framework for web application development
* pytest: framework for testing Python projects
* Jinga2 - templating engine
* SQLAlchemy - ORM (Object Relational Mapper)
* Flask-Bcrypt - password hashing
* Flask-Login - support for user management
* Flask-WTF - simplifies forms

This application is written using Python 3.9.

## Testing

To run all the tests:

```sh
(venv) $ python -m pytest -v
```

To check the code coverage of the tests:

```sh
(venv) $ python -m pytest --cov-report term-missing --cov=project
```
