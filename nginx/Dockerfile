# From https://hub.docker.com/_/nginx/

# Based on nginx 1.11.3
FROM nginx:1.11.3

MAINTAINER Taavi Teska, taaviteska@gmail.com

# Copy the configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Default command
CMD ["nginx", "-g", "daemon off;"]
