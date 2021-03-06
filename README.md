# OAuth 2.0 - Udacity ud330 - Authentication & Authorization

[![Known Vulnerabilities](https://snyk.io/test/github/mramshaw/OAuth2.0/badge.svg?style=plastic&targetFile=requirements.txt)](https://snyk.io/test/github/mramshaw/OAuth2.0?style-plastic&targetFile=requirements.txt)

Another course from __Udacity__ which explains the use of __OAuth 2.0__ (updated here to __v2__).

__OAuth__ is an open standard for authorization which allows for "delegated access" via a third-party authentication service (referred to as an _"__identity provider__"_). This avoids having to log into the service in question. It has also been known as __SSO__ (single sign-on) or ___federated identity___. There can be multiple OAuth paths; the one used here does not involve any __refresh tokens__ (which are optional).

The server-side code is __python__ (using the __Flask__ framework with __sqlalchemy__) while the client-side code is __javascript__ with __jquery__ and __ajax__.

This version of things assumes the current __Ubuntu LTS__ (16.04). It does not use __Vagrant__, which simplifies things quite a bit.

The key functions implemented were the __login__ (with Google) and __logout__ features.

## Updates (as of July 2017)

The version supplied uses __sqlite3__ so neither __postgres__ nor __python-psycopg2__ is needed.

All of the various components were updated to their current __Ubuntu LTS__ (16.04) equivalents.

#### apt-get

The following packages are needed:

	$ sudo apt-get install python-pip python-sqlalchemy

[This will probably require a host of dependencies to be installed.]

#### pip

The various Python components may be installed/upgraded as follows:

	$ pip install --upgrade pip
	$ pip install Werkzeug
	$ pip install Flask
	$ pip install oauth2client
	$ pip install requests
	$ pip install httplib2

[It may be necessary to install additional dependencies as well.]

#### Flask-Login

Installing this into a single-user system was problematic, the following worked:

	$ pip install --user Flask-Login

[It may be necessary to install additional dependencies as well.]

#### Current Versions

These are as follows:

* Python 2.7.12
* sqlite3 3.11.0

The Python components are as follows:

Component | Version
--------- | -------
Flask        | 0.12.2
Flask-Login  | 0.4.0
httplib2     | 0.10.3
pip          | 9.0.1
oauth2client | 4.1.2
requests     | 2.18.1
Werkzeug     | 0.12.2

#### jquery

Updated from __1.8.2__ to __3.2.1__.

#### Google OAuth 2.9

Updated from __v1__ to __v2__.

## Get the Source Code

Download __OAuth2.0-master.zip__ and unzip it into a directory of your choosing.

Or from a terminal, run:

    git clone https://github.com/mramshaw/OAuth2.0.git

#### Git

To install __git__: [download Git from git-scm.com](http://git-scm.com/downloads) and install the version for your operating system.

## Running the Restaurant Menu App

Open a terminal. Type the following:

	$ ls -al

Verify that you are inside the directory that contains two directories named 'templates' and 'static' as well as:

* database_setup.py
* lotsofmenus.py
* project.py

#### Initialization

Initialize the database:

	$ python database_setup.py

[Optional] Populate the database with restaurants and menu items:

	$ python lotsofmenus.py

#### Running

Run the Flask web server [Ctrl-C to terminate]:

	$ python project.py

Open the following link in a web browser to view the restaurant application:

	http://127.0.0.1:5000

The web browser of choice for testing this application is probably __chrome__ (known as __chromium__ on linux).

#### Testing

You should be able to view restaurants and menu items.

You should be able to log in (with Google) and log out.

Once logged in, you should be able to:
* Create restaurants
* Edit or Delete restaurants you have created
* Create, Edit, or Delete menu items for restaurants you have created

## To Do

- [ ] Implement GitHub as an identity provider.
- [ ] Implement BitBucket as an identity provider.
- [ ] Refactor code to more easily accomodate different identity providers.
- [ ] Refactor dependencies into a `requirements.txt` file. 
- [ ] Verify code with Python 3 and `pip3`.

## Credits

Based upon:

	https://www.udacity.com/course/authentication-authorization-oauth--ud330

The course materials are available here:

	https://github.com/udacity/OAuth2.0

Of course, to really learn OAuth it is probably best to follow the course!
