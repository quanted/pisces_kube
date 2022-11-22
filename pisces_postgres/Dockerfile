FROM postgis/postgis:11-2.5-alpine

ARG APP_USER=postgres

RUN apk update
RUN apk upgrade
RUN apk install git

RUN mkdir /tmp
RUN cd /tmp ;
RUN tar -xzf /tmp/postgis-9.6.8.tar.gz
RUN cd /tmp/postgis-9.6.8

RUN mkdir /docker-entrypoint-initdb.d/sql

RUN chown -R $APP_USER:$APP_USER /docker-entrypoint-initdb.d/
RUN chown -R $APP_USER:$APP_USER /docker-entrypoint-initdb.d/sql

USER $APP_USER
