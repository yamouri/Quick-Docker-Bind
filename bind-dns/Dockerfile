FROM debian:latest

RUN apt-get update && apt-get install -y bind9 bind9utils dnsutils \
    && rm -rf /var/lib/apt/lists/*

COPY named.conf.options /etc/bind/named.conf.options
COPY named.conf.local /etc/bind/named.conf.local
COPY db.root /etc/bind/db.root

EXPOSE 53/udp 53/tcp

CMD ["named", "-g", "-c", "/etc/bind/named.conf"]
