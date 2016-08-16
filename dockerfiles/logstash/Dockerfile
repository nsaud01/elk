FROM debian:jessie
RUN apt-get update && \
    apt-get install -y wget git
RUN wget https://download.elastic.co/logstash/logstash/packages/debian/logstash_2.3.4-1_all.deb -O /tmp/logstash.deb && \
 #   git clone https://github.com/logstash-plugins/logstash-output-elasticsearch.git && \
  #  wget https://download.elastic.co/logstash/logstash/packages/debian/logstash-all-plugins_2.3.4-1_all.deb -O /tmp/logstash-contrib.deb && \
    dpkg -i /tmp/logstash.deb ; \
  #  dpkg -i /tmp/logstash-contrib.deb ; \
    apt-get -f -y install && \
    rm -rf /tmp/logstash.deb
COPY logstash.sample.conf /etc/logstash.sample.conf
ENTRYPOINT ["/opt/logstash/bin/logstash"]
CMD []
