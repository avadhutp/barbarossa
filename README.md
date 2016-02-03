## avadhutp/ibex
![ibex](http://dockeri.co/image/avadhutp/ibex)

1. Used for testing [anemometer](https://github.com/box/Anemometer)—a MySQL slow query log analyser
2. To pull: `docker pull avadhutp/ibex`
3. To start, specify a port to map for container's port {{80}}. For example `docker run -p 2050:80 -d avadhutp/ibex`
4. To see anemometer in action, go to `http://your-docker-host-ip:2050/anemometer`
