## avadhutp/ibex
[![ibex](http://dockeri.co/image/avadhutp/ibex)](https://hub.docker.com/r/avadhutp/ibex/)

1. Used for testing [anemometer](https://github.com/box/Anemometer)—a MySQL slow query log analyser
2. Copy `dockerfiles/ibex/conf/sample.config.inc.php` to `dockerfiles/ibex/conf/config.inc.php`.
3. Modify `dockerfiles/ibex/conf/config.inc.php` and add in the database location/credentials/etc. to have your container connect to the correct anemometer db instance.
4. To start, specify a port to map for container's port `8888`. For example `docker run -p 2050:8888 -d avadhutp/ibex`
5. To see anemometer in action, go to `http://your-docker-host-ip:2050`

## avadhutp/amberjack
[![ibex](http://dockeri.co/image/avadhutp/amberjack)](https://hub.docker.com/r/avadhutp/amberjack/)

1. Runs [lazarus](https://github.com/avadhutp/lazarus)—a terminal-based music app written in go 
