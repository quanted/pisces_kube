FROM postgis/postgis:9.6-2.5-alpine

RUN apk update
RUN apk upgrade

ARG APP_USER=postgres
RUN mkdir /docker-entrypoint-initdb.d/sql

RUN chown -R $APP_USER:$APP_USER /docker-entrypoint-initdb.d/
RUN chown -R $APP_USER:$APP_USER /docker-entrypoint-initdb.d/sql

USER $APP_USER
