
## Install Kibana
```
sudo dpkg -i kibana-6.0.0-amd64.deb
```

## To set Kibana to automatically start at boot at start it running, run the following commands:
```
sudo systemctl enable kibana.service
sudo service kibana start
```

## By default, Kibana listens on port 5601, to confirm Kibana has started, open Firefox and navigate to
```
http://localhost:5601.
```
