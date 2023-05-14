FROM python:2.7-buster

MAINTAINER AbdoulAFall (abdoulazizfall2@gmail.com)

ADD student_age.py /

ADD student_age.json /data/

RUN apt-get update && apt-get install -y \
    python-dev \
    python3-dev \
    libsasl2-dev \
    libldap2-dev \
    libssl-dev \
    && pip install flask==1.1.2 \
    flask_httpauth==4.1.0 \
    flask_simpleldap \
    python-dotenv==0.14.0
    
VOLUME /myvolume

EXPOSE 5000

CMD [ "python", "./student_age.py" ]      