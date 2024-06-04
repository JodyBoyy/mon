#set nginx base image
# FROM nginx:1.18
FROM jonasal/nginx-certbot:latest


# create userpass file fot restricted contents
RUN apt-get update && apt-get install -y apache2-utils
RUN htpasswd -b -c /etc/nginx/.htpasswd admin EE268380$585e63b612A

#create folder for giving access to certs
RUN mkdir -p /etc/nginx/ssl

# copy nginx custom configuration file to nginx configs
COPY nginx.conf /etc/nginx/nginx.conf
COPY general.conf /etc/nginx/general.conf
COPY mime.types /etc/nginx/mime.types
# COPY cors.conf /etc/nginx/cors.conf

# copy other configuration
ADD conf.d /etc/nginx/conf.d
# ADD sites-enabled /etc/nginx/sites-enabled

# test commands
# RUN /usr/sbin/nginx -t -c /etc/nginx/nginx.conf
