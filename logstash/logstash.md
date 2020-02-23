## Install Logstash
```
sudo dpkg -i logstash-6.2.1.deb
```

## Set Logstash to not start on boot
```
systemctl is-enabled logstash.service
```

## Tune Logstash settings
```
sudo leafpad /etc/logstash/jvm.options
```

## Change the minimum amount of RAM from 256 MB to 384 MB. Do this by changing 
the file to look like this: 
```
-Xms384m
-Xmx1g
```

## run logstash
```
cd /usr/share/logstash
sudo bin/logstash --path.settings=/etc/logstash -f manual.conf
```
