# Derived from official mysql image (our base image)
FROM mysql:latest
# Add a database
RUN CREATE DATABASE newdb;
RUN USE newdb;
# Add the content of the .sql file to your image
COPY . .
# All scripts in docker-entrypoint-initdb.d/ are automatically
# executed during container startup
