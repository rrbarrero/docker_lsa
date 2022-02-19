FROM debian:bullseye

MAINTAINER Roberto Rodríguez "rbarrero@posteo.net"

RUN apt-get update

RUN apt-get install -y uwsgi uwsgi-plugin-python3 python3-pip libmariadb-dev

COPY requirements.txt /data/
RUN pip install --no-cache-dir -r /data/requirements.txt

COPY uwsgi.ini /data

WORKDIR /data

CMD ["uwsgi", "--ini", "uwsgi.ini"]