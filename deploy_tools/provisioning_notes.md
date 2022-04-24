Provisioning a new site
========================

## Required packages:

* nginx 20.4
* python 3.9
* virtualenv + pip
* Git

eg, on Ubuntu:

	sudo add-apt-repository ppa:fkrull/deadsnakes
	sudo apt-get install nginx git python3.9 python3.9-venv

## Nginx Virtual Host config

* see nginx.template.conf
* replace SITENAME with, e.g., staging.my-domain.com

## Systemd service

* see gunicorn-systemd.template.service
* replace SITENAME with, e.g., staging.my-domain.com

## Folder structure:
Assume we have a user account at /home/username

/home/username
|____sites
		|____SITENAME
				|----database
				|----source
				|----static
				|____virtualenv


				