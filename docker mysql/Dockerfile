# cat Dockerfile
FROM mysql:latest

MAINTAINER baeldung.com

RUN chown -R mysql:root /var/lib/mysql/

ARG studentapp
ARG student
ARG Redhate123
ARG Redhate123

ENV MYSQL_DATABASE=$studentapp
ENV MYSQL_USER=$student
ENV MYSQL_PASSWORD=$Redhate123
ENV MYSQL_ROOT_PASSWORD=$Redhate123

COPY student.sql /etc/mysql/student.sql

RUN sed -i 's/st/'$MYSQL_DATABASE'/g' /etc/mysql/student.sql
RUN cp /etc/mysql/student.sql /docker-entrypoint-initdb.d

EXPOSE 3306

CMD /bin/bash