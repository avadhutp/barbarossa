## avadhutp/ibex
[![ibex](http://dockeri.co/image/avadhutp/ibex)](https://hub.docker.com/r/avadhutp/ibex/)

1. Used for testing [anemometer](https://github.com/box/Anemometer)—a MySQL slow query log analyser
2. To start, specify a port to map for container's port `80`. For example `docker run -p 2050:80 -d avadhutp/ibex`
3. To see anemometer in action, go to `http://your-docker-host-ip:2050/anemometer`

## avadhutp/amberjack
[![ibex](http://dockeri.co/image/avadhutp/amberjack)](https://hub.docker.com/r/avadhutp/amberjack/)

1. Runs [lazarus](https://github.com/avadhutp/lazarus)—a terminal-based music app written in go 