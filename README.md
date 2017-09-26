# Linux Server Configuration

Public IP: 34.205.174.39

SSH Port: 2200

URL (to hosted app): http://34.205.174.39/

Softrware installed: finger, python2, postgresql, virtualenv, nginx, supervisor
In virtualenv: flask and flask libraries, gunicorn

Configuration changes:
- create Unix user for managing web application
- set up postgres and create db user for accessing project db
- clone git repo to `/webapps/brewlocker_local/brewlocker`
- set up environment for the app with virtualenv `/webapps/brewlocker_local/`
- install gunicorn and write script for starting server `/webapps/brewlocker/bin/gunicorn_start`
- install supervisor to autorestart gunicorn instance
- set up nginx as proxy

3rd party resources: I've used some good ideas from [this article](http://michal.karzynski.pl/blog/2013/06/09/django-nginx-gunicorn-virtualenv-supervisor/)

The app is not configured yet to run on https, so OAUTH2 is problematic.

Grader has sudo privileges to run cat and ls commands without password.

