# Dockerfile for Elasticsearch data volume.

FROM ubuntu

# We need to create the Elasticsearch user.
RUN useradd -d "/home/elasticsearch" -m -s /bin/bash elasticsearch

VOLUME /var/log/elasticsearch
VOLUME /usr/share/elasticsearch/config
VOLUME /usr/share/elasticsearch/config/scripts
VOLUME /usr/share/elasticsearch/data
VOLUME /usr/share/elasticsearch/plugins

# Required config files.
ADD ./elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml
ADD ./log4j2.properties /usr/share/elasticsearch/config/log4j2.properties

USER elasticsearch

CMD ["echo", "Data volume for Elasticsearch"]
