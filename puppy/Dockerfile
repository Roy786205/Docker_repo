
#we are placing a base for our docker image
FROM ubuntu:latest
#we are labeling our docker image here
LABEL image="frontendstatic"
#we are running few commands in our container(during container creation)
RUN apt update 
RUN apt install apache2 -y
RUN rm -rf /var/www/html/index.html
COPY puppy* /var/www/html/
WORKDIR /var/www/html
#we are exposing our container to a port
EXPOSE 80
#we are providing container a processs 
CMD ["apachectl", "-D" ,"FOREGROUND"]