# elk-reporting-module
Configure Filebeat

We can find filebeat configuration file at :/etc/filebeat/filebeat.yml

Step 1 :Define the path (or paths) to your log files.

filebeat.inputs:
- type: log
  enabled: true
  paths:
    - /var/log/*.log

Step 2 : If you want to use Logstash to perform additional processing on the data collected by Filebeat, you need to configure Filebeat to use Logstash.

Please copy the Logstash configuration file at: /etc/logstash/conf.d/cars.conf or logstash/config

Start logstash with configuration file

sudo ./logstash -f ../config/nuwan.conf

