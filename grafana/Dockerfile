#FROM grafana/grafana:4.4.2
#fron alpine image
FROM grafana/grafana:6.4.0-beta1

#ARG SSL_KEYSTORE_PASSWORD
#USER root


#RUN apt-get update && apt-get install -y curl gettext-base && rm -rf /var/lib/apt/lists/*

RUN apk update && apk upgrade && apk install -y curl gettext-base && rm -rf /var/lib/apt/lists/*

#RUN apt-get update
#RUN apt-get install -y curl gettext-base
#RUN rm -rf /var/lib/apt/lists/*

WORKDIR /etc/grafana
COPY datasources ./datasources

WORKDIR /app
COPY entrypoint.sh ./
#RUN chmod u+x entrypoint.sh
RUN ls /app/
ENTRYPOINT ["/app/entrypoint.sh"]
#RUN ["chmod", "u+x", "/app/entrypoint.sh"]
#USER 1001

