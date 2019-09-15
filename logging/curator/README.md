#Elasticsearch v7 Curator Logstash indices retention cron job

###Prerequisite
- Before deploying curator stack you should create curator image by using Th Docker file which exist in this directory as below:

**docker build -t registry.local/curator:5.7.6

```
You can set the cron `PERIOD` to 15min, hourly, daily, weekly and monthly.

The default index pattern is `[prefix-]%Y.%m.%d`.
