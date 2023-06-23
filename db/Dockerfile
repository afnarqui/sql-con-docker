FROM mcr.microsoft.com/mssql/server:2019-CU3-ubuntu-18.04

ENV ACCEPT_EULA=Y \
    MSSQL_SA_PASSWORD=quintero1.

WORKDIR /init
COPY init-db.* ./
USER root
RUN chmod +x ./init-db.sh
RUN /opt/mssql/bin/sqlservr & ./init-db.sh
