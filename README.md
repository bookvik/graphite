# graphite

docker run \
 --net=host --privileged \
 -v /:/hostfs:ro \
 -e HOST_NAME=myhost \
 -e GRAPHITE_HOST=your.graphite.com \
 --name collectd pboos/collectd-graphite
 
 docker run -d --name graphite --restart=always -p 8081:80 -p 2003-2004:2003-2004 -p 2023-2024:2023-2024 -p 8125:8125/udp -p 8126:8126 graphiteapp/graphite-statsd
