# Use python as base image
FROM python:3.7
# Install apt dependencies
RUN  apt-get update
RUN  apt-get install python3 -y
RUN  apt-get install python3-pip -y
# Copy everything from the app
COPY . .
# Install dependencies
RUN pip3 install Flask
RUN pip3 install pymysql 
RUN pip3 install flask_sqlalchemy 
RUN pip3 install jinja2 
# Expose correct port
EXPOSE 5000
# Create entrypoint
ENTRYPOINT ["python", "app.py"]







