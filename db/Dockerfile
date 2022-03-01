# Use mysql 5.7 as the flask-app is not set up to work with later versions
FROM mysql:5.7
# Add a database and root password
ENV MYSQL_DATABASE=flask-db
ENV MYSQL_ROOT_PASSWORD=root
# Add the content of the .sql file to your image
# All scripts copied to docker-entrypoint-initdb.d/ are automatically
# executed during container startup
WORKDIR /trio-task/flask-app/db/
COPY CreateTable.sql /docker-entrypoint-initdb.d/