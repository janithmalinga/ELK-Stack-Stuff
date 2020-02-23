## Install elasticsearch--------
```
sudo dpkg -i elasticsearch-6.0.0.deb
```

You should see the following output
```
(Reading database ... 226016 files and directories currently
installed.)
Preparing to unpack .../elasticsearch-6.0.0.deb ...
Creating elasticsearch group... OK
Creating elasticsearch user... OK
Unpacking elasticsearch (6.0.0) ...
Setting up elasticsearch (6.0.0) ...
Processing triggers for systemd (229-4ubuntu19) ...
Processing triggers for ureadahead (0.100.0-19) ...
```
## Configure elasticsearch
```
sudo gedit /etc/elasticsearch/elasticsearch.yml
```
Remove the "#" from the front of the cluster.name, node.name, and node.attr.rack. 
Then, change the cluster.name parameter from "my-application" to "egs101". 
The node.name parameter can remain as "node-1". Change the line with the 
node.attr.rack parameter to read "node.attr.box_type: hot". Finally, add a new line 
that says "path.repo: ["/labs/backups/"]" as shown below. 
The file should now look like this:

Please Note: make sure /labs/backups/ folder is created and give permissions.

## Change Elasticsearch Java settings
```
sudo gedit /etc/elasticsearch/jvm.options
```
Change the both the -Xms and -Xmx settings to 1100MB
```
-Xms1100m
-Xmx1100m
```
## Start Elasticsearch
```
sudo service elasticsearch start
sudo service elasticsearch status
```

## Access Elasticsearch

## Open firefox browser and goto 
```
http://localhost:9200
```

## Elasticsearch Error log
```
/var/log/elasticsearch or /var/log/syslog
```
