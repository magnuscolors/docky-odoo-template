FROM camptocamp/odoo-project:14.0-latest-batteries
MAINTAINER Magnus

# Project's specifics packages
RUN set -x; \
        apt-get update \
        && apt-get install -y --no-install-recommends \
        python-shapely git \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/*

COPY ./requirements.txt /odoo/
RUN cd /odoo && pip install -r requirements.txt

ENV DB_NAME = app_backend01
    DBFILTER = app_backend01
    LIST_DB=True \
    ADMIN_PASSWD = ButNoS1mpler
# DEMO=False \
    LIMIT_TIME_CPU=60000 \
    LIMIT_TIME_REAL=120000 \
    DB_HOST=db10 \
    ADDONS_PATH=/odoo/local-src,/odoo/src/addons,/odoo/external-src/calendar,/odoo/external-src/connector-interfaces,/odoo/external-src/connector,/odoo/external-src/data-protection,/odoo/external-src/geospatial,/odoo/external-src/multi-company,/odoo/external-src/reporting-engine,/odoo/external-src/rest-framework,/odoo/external-src/server-auth,/odoo/external-src/web,/odoo/external-src/webkit-tools,/odoo/external-src/queue,/odoo/external-src/server-tools,/odoo/external-src/server-ux,/odoo/external-src/server-backend,/odoo/external-src/odoo-usability,/odoo/external-src/ak-odoo-incubator
