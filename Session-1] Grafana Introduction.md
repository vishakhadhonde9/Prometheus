# Grafana -
- Grafana is an open-source data visualization and monitoring tool used for analyzing and displaying metrics from various data sources.

# Features of Grafana:
## Data Visualization:
- Create dashboards with charts, graphs, heatmaps, tables, etc.
- Real-time updates with auto-refresh.

## Multiple Data Sources:
- Supports Prometheus, InfluxDB, Graphite, Elasticsearch, MySQL, PostgreSQL, Loki (for logs), and more.

## Alerting:
- Set alert rules on your metrics and get notified via email, Slack, PagerDuty, etc.

## Custom Dashboards:
- Drag-and-drop interface to build your own dashboard.
- Share dashboards via links or snapshots.

# Prometheus Configuration -

      sudo rpm --import https://packages.grafana.com/gpg.key
      
- copy these all lines and execute as one command

sudo tee /etc/yum.repos.d/grafana.repo <<EOF
[grafana]
name=grafana
baseurl=https://packages.grafana.com/oss/rpm
repo_gpgcheck=1
enabled=1
gpgcheck=1
gpgkey=https://packages.grafana.com/gpg.key
sslverify=1
sslcacert=/etc/pki/tls/certs/ca-bundle.crt
EOF


    sudo yum install grafana -y
    sudo systemctl start grafana-server
    sudo systemctl enable grafana-server
    sudo systemctl status grafana-server


- copy public ip and paste on broswer

      http://pub-ip:3000






