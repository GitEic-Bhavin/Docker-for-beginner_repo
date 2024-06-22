FROM ubuntu
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip
RUN rm /usr/lib/python3.*/EXTERNALLY-MANAGED
RUN pip3 install flask
RUN pip3 install flask-mysql

COPY app.py /opt/app.py

ENTRYPOINT FLASK_APP=/opt/app.py flask run --host=0.0.0.0
