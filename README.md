# PROMGRAF
Prometheus, Grafana, Node-Exporter and cAdvisor one-host Docker containers with Nginx as frontend.

### Configure Grafana
Grafana container has a bind of /etc/grafana/grafana.ini to ./Grafana/grafana.ini. You can change Grafana settings by editing it. Please read [Configure a Grafana Docker image](https://grafana.com/docs/grafana/v9.0/setup-grafana/configure-docker/#configure-a-grafana-docker-image) first.

### Prometheus Node Exporter
To enable host system monitoring Node Exporter has to be run on it, but not as container. Be sure to protect world access to your Node Exporter metrics. It can be made via startup option --web.listen-address=":9100", or via firewall. I prefer the last because it more easy  to restrict world access there than setting particular IP address in option.  
