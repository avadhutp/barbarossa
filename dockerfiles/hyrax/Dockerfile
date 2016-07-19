FROM node:argon

MAINTAINER avadhutp

LABEL description="Running phantomas for testing"

# Install basic dependencies
RUN \
	apt-get update && \
	apt-get install -y jq && \
	apt-get install -y vim

# Install phantom
RUN npm install --global phantomjs phantomas