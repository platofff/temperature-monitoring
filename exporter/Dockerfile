FROM debian:bullseye-slim
WORKDIR /exporter
ADD ./ /exporter
RUN apt-get update; \
apt-get install -y --no-install-recommends python3-pip lighttpd; \
pip3 install -r /exporter/requirements.txt
ADD ./lighttpd.conf /etc/lighttpd/lighttpd.conf
CMD [ "lighttpd", "-D", "-f", "/etc/lighttpd/lighttpd.conf" ]
