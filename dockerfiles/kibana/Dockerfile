FROM nginx:1
RUN apt-get update && apt-get install -y wget ca-certificates
RUN wget https://download.elastic.co/kibana/kibana/kibana-4.5.4-linux-x64.tar.gz -O /tmp/kibana.tar.gz && \
    cd /tmp && tar zxf kibana.tar.gz && mv kibana-*/* /usr/share/nginx/html/
EXPOSE 80
