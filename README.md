# StaTSDB
Files needed to setup Statsd with an OpenTSDB backend on Zenoss Control Center
Initial release 0.0.7
Dockerfile so you can build your own centos 6, statsd with opentsdb backend.
Just change the host information as needed before building.

# INSTALLING on the Zenoss Command Center Server
Clone the git repo to a a directory of your choice. (/usr/src/, /tmp/)
then run the build command:

docker build -t aquinn/statsdb:0.7 -f ./DockerFile .

Then use the Zenoss Command Center webui to add the application template 'statsdb.json', then add a new application using the statsdb template.
You may have to change some of the settings but this initial commit will get you 90+% to a working statsd ingest into opentsdb for zenoss.
