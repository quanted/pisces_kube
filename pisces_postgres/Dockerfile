FROM postgis/postgis:11-3.3-alpine

ARG APP_USER=postgres

RUN apk update
RUN apk upgrade

RUN mkdir /docker-entrypoint-initdb.d/sql

RUN chown -R $APP_USER:$APP_USER /docker-entrypoint-initdb.d/
RUN chown -R $APP_USER:$APP_USER /docker-entrypoint-initdb.d/sql

USER $APP_USER
