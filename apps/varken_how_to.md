# GUIDE FOR DEPLOYING INFLUX, GRAFANA AND VARKEN ON PLEXGUIDE
# AUTHOR: BENDER


CD to /opt/mycontainers

First, grab the templates
wget https://raw.githubusercontent.com/benderstwin/PlexGuide-Community/v8.4/apps/bender-influx.yml
wget https://raw.githubusercontent.com/benderstwin/PlexGuide-Community/v8.4/apps/bender-varken.yml
wget https://raw.githubusercontent.com/benderstwin/PlexGuide-Community/v8.4/apps/bender-grafana.yml

Set up the influx credentials
nano /opt/mycontainers/bender-influx.yml

set the influx username and password in the template

Change these lines:

INFLUX_ADMIN_USER: 'influxdbadmin'
INFLUX_ADMIN_PASSWORD: 'influxdbpass'

deploy bender-influx, bender-grafana and bender-varken through plexguide (community)

edit your varken.ini file
sudo nano /opt/appdata/varken/varken.ini

Instructions to configure are not part of this howto but are located here https://github.com/Boerderij/Varken/wiki/Configuration
You should be able to use the container name for anything on the same host (IE influx, ombi, sonarr etc...)

Like this and want to buy me a beer, I'm cool with that https://beerpay.io/benderstwin/benders-scripts
Thanks!