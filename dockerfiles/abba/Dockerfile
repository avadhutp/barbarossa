FROM ubuntu:14.04

MAINTAINER avadhutp

LABEL description="To test out uWSGI + mod_proxy_uwsgi."

# Install basic dependencies
RUN \
	apt-get update && \
    apt-get install -y build-essential python-dev python-setuptools apache2 apache2-mpm-event libapache2-mod-proxy-uwsgi && \
    easy_install pip && \
    pip install uwsgi

# Put in the code
ADD dockerfiles/abba/src/ /

# configure apache
RUN \
	a2enmod proxy && \
	sed -i 's/Listen 80/Listen 8888/g' /etc/apache2/ports.conf && \
	rm /etc/apache2/sites-enabled/000-default.conf

COPY dockerfiles/abba/conf/mod_proxy_uwsgi_virtualhost.conf /etc/apache2/sites-enabled/000-uwsgi.conf

# Glue everything together
CMD \
	service apache2 restart && \
	uwsgi --socket 127.0.0.1:2050 --wsgi-file foo.py

EXPOSE 8888
