#Use Python 3.6 as a base image
FROM python:3.6
# Copy contents into image
WORKDIR /trio-task/flask-app/
COPY app.py /flask-app/
COPY templates /flask-app/templates/
# install pip dependencies from requirements file
COPY requirements.txt /tmp/requirements.txt
RUN pip3 install -r /tmp/requirements.txt
# Expose correct port
EXPOSE 5000
# Create an entrypoint
ENTRYPOINT ["python3", "/flask-app/app.py"]