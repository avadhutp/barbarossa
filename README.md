## avadhutp/ibex
[![ibex](http://dockeri.co/image/avadhutp/ibex)](https://hub.docker.com/r/avadhutp/ibex/)

1. Used for testing [anemometer](https://github.com/box/Anemometer)—a MySQL slow query log analyser
1. Copy `dockerfiles/ibex/conf/sample.config.inc.php` to `dockerfiles/ibex/conf/config.inc.php`.
1. Modify `dockerfiles/ibex/conf/config.inc.php` and add in the database location/credentials/etc. to have your container connect to the correct anemometer db instance.
1. To start, specify a port to map for container's port `8888`. For example `docker run -p 2050:8888 -d avadhutp/ibex`
1. To see anemometer in action, go to `http://your-docker-host-ip:2050`

## avadhutp/amberjack
[![ibex](http://dockeri.co/image/avadhutp/amberjack)](https://hub.docker.com/r/avadhutp/amberjack/)

1. Runs [lazarus](https://github.com/avadhutp/lazarus)—a terminal-based music app written in go 

## avadhutp/springhare
[![springhare](http://dockeri.co/image/avadhutp/springhare)](https://hub.docker.com/r/avadhutp/springhare/)

1. Runs [query_monitor](https://github.com/avadhutp/query_monitor)—a collection of recipes running atop [anemometer](https://github.com/box/anemometer)
1. Before you begin, make sure you rename and modify the `conf/query_monitor.yaml.example` to `conf/query_monitor.yaml`.
1. How to run: `docker run -t avadhutp/springhare`

| Command | description |
|---------|-------------|
| `healthcheck` | Runs checks to see if anemometer, jira, and other associated systems are working correctly. |
| `frequency_check` | Identifies frequency queries. For more options for this command [see this](https://github.com/avadhutp/query_monitor#frequency_check). |

