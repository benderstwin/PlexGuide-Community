#####  HOW TO SET UP TELEGRAF ON PLEXGUIDE  #####

Do all of the following as root, or sudo

1.  Create the directory /opt/appdata/telegraf
    ```mkdir /opt/appdata/telegraf```

2.  Change to the telegraf directory and download config<br>
    ```cd /opt/appdata/telegraf```
    <br>
    ```wget https://raw.githubusercontent.com/benderstwin/PlexGuide-Community/v8.4/apps/telegraf.conf```

3.  change to the mycontainers directory and download template<br>
    ```cd /opt/mycontainers```
    <br>
    ```wget https://raw.githubusercontent.com/benderstwin/PlexGuide-Community/v8.4/apps/bender-telegraf.yml```

4.  edit the telegraf.conf to add your influxdb username and password<br>
    ```nano /opt/appdata/telegraf.conf```
    Look for these lines (around line 116)
    ```## HTTP Basic Auth
        username = "telegraf"
        password = "metricsmetricsmetricsmetrics"```

        Modify with your own influx username and password.  Save the file.

5.  deploy bender-telegraf throuh plexguide community apps
6.  add the datasource to grafana, import or create a dashboard, profit.

Like this and want to buy me a beer? I'm cool with that https://beerpay.io/benderstwin/benders-scripts
Thanks!
