#FROM grafana/grafana:6.4.0-beta1
FROM grafana/grafana:4.4.2

RUN apt-get update && apt-get install -y curl gettext-base && rm -rf /var/lib/apt/lists/*

WORKDIR /etc/grafana
COPY datasources ./datasources

WORKDIR /app
COPY entrypoint.sh ./
RUN chmod u+x entrypoint.sh
RUN ls /app/
ENTRYPOINT ["/app/entrypoint.sh"]
