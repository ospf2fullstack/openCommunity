FROM redhat/ubi8:latest

RUN yum update -y

RUN yum install -y nginx

# copyin nginx configuration file
COPY ./source/nginx.conf /etc/nginx/nginx.conf

# copy in static website 
COPY ./source/www/ /usr/share/nginx/html/

EXPOSE 8080

CMD [ "nginx","-g", "daemon off;" ]