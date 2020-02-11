FROM magnuscolors/odoo-project:10.0-debian-stretch-batteries
MAINTAINER Magnus

# Project's specifics packages
RUN DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get install -y python-shapely git vim && \
    apt-get clean

COPY ./requirements.txt /odoo/
RUN cd /odoo && pip install -r requirements.txt

ENV LIST_DB=True
ENV LIMIT_TIME_CPU=6000
ENV LIMIT_TIME_REAL=12000
ENV ADDONS_PATH=/odoo/local-src,/odoo/src/addons,/odoo/links

