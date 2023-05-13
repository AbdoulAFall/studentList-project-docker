FROM python:2.7-buster

MAINTAINER AbdoulAFall (abdoulazizfall2@gmail.com)

COPY student_age.py /root/

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
    
VOLUME myvolume /root/

EXPOSE 5000

CMD [ "python", "./student_age.py" ]
