# From https://hub.docker.com/_/nginx/

# Based on nginx 1.13.3
FROM nginx:1.13.3

MAINTAINER Taavi Teska, taaviteska@gmail.com

# Copy the configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Copy the default page
COPY default.html /var/www/default/htdocs/index.html

# Default command
CMD ["nginx", "-g", "daemon off;"]
