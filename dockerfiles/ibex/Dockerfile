FROM ubuntu:14.04

MAINTAINER avadhutp

LABEL description="To test out anemometer+mysql monitoring; especially, slow query log."

# Install basic dependencies
RUN \
    apt-get install -y git && \
    apt-get install -y emacs && \
    apt-get install -y openssh-server apache2 php5 php5-cli libapache2-mod-php5 php5-gd php5-json php5-mysql

# Install MySQL
RUN \ 
    apt-get update && \
    apt-get install -y mysql-server && \
    apt-get install -y mysql-client

# Install percona-toolkit    
RUN \
    apt-key adv --keyserver keys.gnupg.net --recv-keys 1C4CBDCDCD2EFD2A && \
    echo "deb http://repo.percona.com/apt `lsb_release -cs` main" > /etc/apt/sources.list.d/percona.list && \
    apt-get update && \
    apt-get install -y percona-toolkit

# Install anemometer
RUN \
    cd /var/www/html && \
    git clone git://github.com/box/Anemometer.git anemometer && \
    cd anemometer && \
    service mysql start && \
    mysql < install.sql && \
    cd conf && \
    cp sample.config.inc.php config.inc.php

# Start stuff
CMD \
    service mysql start && \
    apachectl -D FOREGROUND

EXPOSE 80