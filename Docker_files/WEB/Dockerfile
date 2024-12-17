FROM nginx

LABEL "project"="vprofile"
LABEL "user"="Raja"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginxvproapp.conf  /etc/nginx/conf.d/vproapp.conf

