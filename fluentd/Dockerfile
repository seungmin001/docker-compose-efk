ARG FLUENTD_VERSION=v1.14-debian-1
FROM --platform=linux/amd64 fluent/fluentd:${FLUENTD_VERSION}

USER root
RUN gem install elasticsearch -v 7.17.0
RUN gem install --no-document fluent-plugin-elasticsearch

USER fluent
