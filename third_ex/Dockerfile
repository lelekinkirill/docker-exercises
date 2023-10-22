FROM ubuntu:18.04
RUN apt-get update && apt-get install -y nginx
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf
WORKDIR /etc/nginx/
VOLUME /var/lib/nginx
ENTRYPOINT ["nginx"]
CMD ["-g", "daemon off;"]
