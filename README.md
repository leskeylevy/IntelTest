# IntelTest
#  Introduction
## Project prompt
The application aims to provide edivendence of mastery of implementation concepts. A user can login in and out of the application.
For the online version use this credentials to login 
Username === TestUser
Password === TestPassword

## Getting Started.
These instructions will get you a copy of the project up and running on a local host.

Step 1: git clone
<br />Step 2: Enter the Project root folder

cd IntelTest/
<br />install virtual environment (venv) without pip

python3.6 -m venv --without-pip virtual
<br />Step 3: Activate virtual environment

<br />source virtual/bin/activate.
<br />install pip using curl.
## Built With
* Python3.6 - Python is a programming language that lets you work quickly and integrate systems more effectively.
* Django - Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design.
* postgresql - PostgreSQL is a powerful, open source object-relational database system with over 30 years of active development that has earned it a strong reputation for reliability, feature robustness, and performance.
## Bugs
The online version of the application is still a work in progress and the ocassional nginx errors are to be expected

## DEPLOYMENT
The aim of this process is to have the app running on a red-hat based linux environment and for our case the environment of choice is CentOs 8

### Preparing your environment
All the sets required for this process are well document on  <a href="https://www.digitalocean.com/community/tutorials/initial-server-setup-with-centos-8">this link</a> here.
Follow the instructions there as the first step

Once your environment is secured with the right permissions for your Users,
Proceed to install packages from EPEL and the CentOs repositories.
First enable the EPEL repo by running <code> sudo yum install epel-release </code>
Proceed to install all depedencies needed using this command
<code>sudo yum install python3-pip python3-devel postgresql-server postgresql-devel postgresql-contrib gcc nginx </code>

### Postgres SetUp for Django
Instructions for setting up Postgres in CentOs can be found <a href="https://www.digitalocean.com/community/tutorials/how-to-set-up-django-with-postgres-nginx-and-gunicorn-on-centos-7">Here!</a>

### Clone this repo 
You can now go ahead and use git to clone this repository  into your environment.
If you don't have git installed check out <a href="https://www.digitalocean.com/community/tutorials/how-to-install-git-on-centos-8">here</a>
Check if there is a Venv folder and delete it.

### Project Environment
After deleting the venv folder we need a virtual environment and we  can achieve this by running <code>sudo pip install virtualenv</code>
Activate your environment <code> source yourprojectenv/bin/activate</code>
Install all dependencies in the requirements.txt file using <code>pip install -r requirements.txt </code>


### Gunicorn And Nginx
Now try running the app using <code> python manage.py runserver 0.0.0.0:8000 <code/> 
Navigate to http://your_environment_Ip_address:8000 and check out your site using a development server.

To move to a production server a combination of gunicorn and Nginx is used (Apache is also a good one but thats for another day).




## Authors
LESKEYLEVY

## License
This project is licensed under the MIT License.

## Acknowledgments
Digital Ocean.
