FROM nginx:stable-alpine3.17-slim

ARG APP_USER=nginx

RUN apk update
RUN apk upgrade
RUN apk upgrade openssl


RUN rm /etc/nginx/conf.d/default.conf

COPY nginx.conf /etc/nginx/conf.d/
