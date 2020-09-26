# nodered-influxdb-mqtt
## Components
- MQTT broker
- InfluxDB
- Node-Red [port: see below]
    - google/alexa, Homematic CCU addons
- Grafana


## Deploy
[![](https://www.balena.io/deploy.png)](https://dashboard.balena-cloud.com/deploy)

## Remarks on node-red
A Node-RED application with [balena-supervisor](https://balena.io/docs/reference/supervisor/supervisor-api/) flow [support](https://github.com/balena-io-projects/node-red-contrib-balena)

### Configure via [environment variables](https://balena.io/docs/learn/manage/serv-vars/)
Variable Name | Default | Description
------------ | ------------- | -------------
NR_PORT | `1880` | the port that exposes the Node-RED UI
USERNAME | `none` | the Node-RED admin username
PASSWORD | `none` | the Node-RED admin password [hash](https://nodered.org/docs/security#generating-the-password-hash)

You **must** set the `USERNAME` and `PASSWORD` environment variables to be able to save or run programs in Node-RED.  
The hash for the `PASSWORD` variable can be generated using the [`node-red-admin`](https://nodered.org/docs/node-red-admin)
command line tool. Instructions for generating a password hash can be found in
the [Node-RED documentation](https://nodered.org/docs/security#generating-the-password-hash).  
More information about using and setting environment variables can be found in
the [balena docs](https://balena.io/docs/learn/manage/serv-vars/).


## remarks on influxdb
create databases via balena dashboard
- connect to container
- connect to influx (create database...)



