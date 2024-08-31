FROM mysql:latest

#set root mysql password
ENV MYSQL_ROOT_PASSWORD=Redhate123

#create database and table upon container
COPY init-db.sql /docker-entrypoint-initdb.d/

#expose the mysql port
EXPOSE 3306

#start the mysql server
CMD [ "mysqld" ]