## Home Assistant

http://192.168.0.11:8123

Executar o home assistant

> `sudo -u homeassistant -H -s`
> `cd /srv/homeassistant`
> `python3.8 -m venv .`
> `source bin/activate`
> `hass`

user: adriano  
pass: baumart77b896
















# PROCEDIMENTOS PARA INSTALAÇÃO DO HOMEASSISTANT #

https://www.home-assistant.io

## Home Assistant Core ##


**INSTALL DEPENDENCIES** 

Before you start make sure your system is fully updated, all packages in this guide are installed with apt, if your OS does not have that, look for alternatives.

> `sudo apt-get update`
> `sudo apt-get upgrade -y`

Install the dependencies:

> `sudo apt-get install -y python3 python3-dev python3-venv python3-pip libffi-dev libssl-dev libjpeg-dev zlib1g-dev autoconf build-essential libopenjp2-7 libtiff5 tzdata`

**CREATE AN ACCOUNT  **  
Add an account for Home Assistant Core called `homeassistant`. Since this account is only for running Home Assistant Core the extra arguments of `-rm` is added to create a system account and create a home directory.

> `sudo useradd -rm homeassistant`

**CREATE THE VIRTUAL ENVIRONMENT**  
First we will create a directory for the installation of Home Assistant Core and change the owner to the `homeassistant` account.

> `sudo mkdir /srv/homeassistant`
> `sudo chown homeassistant:homeassistant /srv/homeassistant`

Next up is to create and change to a virtual environment for Home Assistant Core. This will be done as the `homeassistant` account.

> `sudo -u homeassistant -H -s`
> `cd /srv/homeassistant`
> `python3.8 -m venv .`
> `source bin/activate`

Once you have activated the virtual environment (notice the prompt change to `(homeassistant) homeassistant@raspberrypi:/srv/homeassistant $)` you will need to run the following command to install a required Python package.

> `python3 -m pip install wheel`

Once you have installed the required Python package it is now time to install Home Assistant Core!

> `pip3 install homeassistant`

Start Home Assistant Core for the first time. This will complete the installation for you, automatically creating the .homeassistant configuration directory in the /home/homeassistant directory, and installing any basic dependencies.

> `hass`

You can now reach your installation via the web interface on http://homeassistant.local:8123.

If this address doesn’t work you may also try http://localhost:8123 or http://X.X.X.X:8123 (replace X.X.X.X with your machines’ IP address).

