FROM python:3.5
WORKDIR /opt/sqggles
COPY requirements.txt requirements.txt
RUN pip install uwsgi -r requirements.txt
COPY . .
RUN groupadd -r -g 999 application && \
    useradd -r -g application application && \
    chown -R application:application .
RUN mkdir /run/sqggles && \
    chown application:application /run/sqggles
VOLUME /opt/sqggles \
       /run/sqggles
CMD uwsgi config/application/uwsgi.ini
