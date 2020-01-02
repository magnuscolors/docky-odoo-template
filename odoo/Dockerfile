FROM magnuscolors/odoo-project:11.0-latest-batteries-onbuild
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

ENV LIST_DB=False \
# DEMO=False \
    LIMIT_TIME_CPU=6000 \
    LIMIT_TIME_REAL=12000 \
    DB_HOST=db \
    ADDONS_PATH=/odoo/local-src,/odoo/src/addons,/odoo/external-src/club3d-addons,/odoo/external-src/account-analytic,/odoo/external-src/account-closing,/odoo/external-src/account-consolidation,/odoo/external-src/account-financial-reporting,/odoo/external-src/account-financial-tools,/odoo/external-src/account-fiscal-rule,/odoo/external-src/account-invoicing,/odoo/external-src/bank-payment,/odoo/external-src/bank-statement-import,/odoo/external-src/calendar,/odoo/external-src/commission,/odoo/external-src/community-data-files,/odoo/external-src/connector-cmis,/odoo/external-src/connector-ecommerce,/odoo/external-src/connector-interfaces,/odoo/external-src/connector-magento,/odoo/external-src/connector-telephony,/odoo/external-src/connector,/odoo/external-src/contract,/odoo/external-src/crm,/odoo/external-src/data-protection,/odoo/external-src/delivery-carrier,/odoo/external-src/donation,/odoo/external-src/e-commerce,/odoo/external-src/edi,/odoo/external-src/event,/odoo/external-src/geospatial,/odoo/external-src/hr-timesheet,/odoo/external-src/hr,/odoo/external-src/knowledge,/odoo/external-src/l10n-netherlands,/odoo/external-src/maintenance,/odoo/external-src/management-system,/odoo/external-src/margin-analysis,/odoo/external-src/multi-company,/odoo/external-src/partner-contact,/odoo/external-src/product-attribute,/odoo/external-src/product-variant,/odoo/external-src/project-agile,/odoo/external-src/project-reporting,/odoo/external-src/project,/odoo/external-src/purchase-reporting,/odoo/external-src/purchase-workflow,/odoo/external-src/intrastat-extrastat,/odoo/external-src/reporting-engine,/odoo/external-src/rest-framework,/odoo/external-src/rma,/odoo/external-src/sale-financial,/odoo/external-src/sale-reporting,/odoo/external-src/sale-workflow,/odoo/external-src/server-auth,/odoo/external-src/social,/odoo/external-src/stock-logistics-barcode,/odoo/external-src/stock-logistics-reporting,/odoo/external-src/stock-logistics-transport,/odoo/external-src/stock-logistics-warehouse,/odoo/external-src/stock-logistics-workflow,/odoo/external-src/vertical-agriculture,/odoo/external-src/vertical-association,/odoo/external-src/vertical-construction,/odoo/external-src/vertical-edition,/odoo/external-src/vertical-education,/odoo/external-src/vertical-isp,/odoo/external-src/vertical-travel,/odoo/external-src/web,/odoo/external-src/webkit-tools,/odoo/external-src/website-cms,/odoo/external-src/account-reconcile,/odoo/external-src/mis-builder,/odoo/external-src/operating-unit,/odoo/external-src/queue,/odoo/external-src/server-tools,/odoo/external-src/server-ux,/odoo/external-src/server-backend,/odoo/external-src/odoo-usability,/odoo/external-src/ak-odoo-incubator

