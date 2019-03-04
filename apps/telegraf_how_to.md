#####  HOW TO SET UP TELEGRAF ON PLEXGUIDE  #####

Do all of the following as root, or sudo

1.  Create the directory /opt/appdata/telegraf<br>
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
    ```nano -c /opt/appdata/telegraf.conf```<br>
        - tip: adding the -c to the nano command will show you the line number at the bottom, makes it easier to find.
    Look for these lines (around line 116) under ```HTTP Basic Auth```
    ``` 
        username = "telegraf"
        password = "metricsmetricsmetricsmetrics"
    ```

        Modify with your own influx username and password.  Save the file.

5.  deploy bender-telegraf throuh plexguide community apps
6.  add the datasource to grafana, import or create a dashboard, profit.
    - When you add the data source, the URL is probably http://influx:8086 and the db name should be telegraf (database should be created for you already)

Like this and want to buy me a beer? I'm cool with that https://beerpay.io/benderstwin/benders-scripts
Thanks!
