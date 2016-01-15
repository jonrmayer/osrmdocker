FROM osrmbase
MAINTAINER Jonathan Mayer <jonathan.mayer@ecountability.co.uk>

# Let the container know that there is no TTY
ENV DEBIAN_FRONTEND noninteractive

RUN mkdir -p /opt/osrm/etc /opt/osrm/bin

ADD sources/ /opt/osrm/bin/

VOLUME ["/opt/osrm/data", "opt/osrm/etc", "opt/osrm/stxxl", "opt/osrm/profiles"]

EXPOSE 5000

ENTRYPOINT ["/opt/osrm/bin/boot"]

CMD ["usr/bin/osrm-routed", "-c", "/opt/osrm/etc/osrm.conf", "/opt/osrm/data/map.osrm"]

