# cat Dockerfile
FROM mysql:latest

MAINTAINER baeldung.com

RUN chown -R mysql:root /var/lib/mysql/

ARG studentapp
ARG student
ARG Redhate123
ARG REd

ENV MYSQL_DATABASE=$MYSQL_DATABASE
ENV MYSQL_USER=$MYSQL_USER
ENV MYSQL_PASSWORD=$MYSQL_PASSWORD
ENV MYSQL_ROOT_PASSWORD=$MYSQL_ROOT_PASSWORD

COPY student.sql /etc/mysql/student.sql

RUN sed -i 's/MYSQL_DATABASE/'$MYSQL_DATABASE'/g' /etc/mysql/student.sql
RUN cp /etc/mysql/student.sql /docker-entrypoint-initdb.d

EXPOSE 3306

CMD /bin/bash