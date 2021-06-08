# Prometheus
Simple docker-compose file in order to launch prometheus/grafana and a snmp_exporter>

## Configuration
The docker file assumes that in the same folder you have:
- a data folder used for prometheus data
- the prometheus.yml configuration file
- a grafana folder used for grafana data
- a snmp folder with a snmp.yml file

Prometheus will be accessible through http://localhost:9090, grafana through http://localhost:3000
and the snmp_exporter through http://localhost:9116.

We you are on the snmp_exporter just put the IP of the server/machine where the snmp deamon runs then
specify the module (e.g: synology if you want to monitor a synology NAS). The snmp.yml has been generated
with the generator tool provide by Prometheus to only have the OID i wanted. A generic file is
provided on their git (see below).  

## link
https://prometheus.io/docs/prometheus/latest/configuration/configuration/  
https://github.com/prometheus/snmp_exporter  
https://grafana.com/docs/grafana/latest/installation/docker/
