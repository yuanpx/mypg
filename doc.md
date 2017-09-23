# ENV
PGHOST PGHOSTADDR
PGPORT
PGDATABASE
PGUSER
PGPASSWORD
PGPASSFILE
PGSYSCONFDIR
PGSERVICEFILE
PGSERVICE
PGDATA

# PATH
~/.pgpass
/etc/pg_service.conf
~/.pg_service.conf

# CONFIG FILE

## postgresql.conf
listen_addresses = '*'

## pg_service.conf
[dbservice]
host=
port=
dbname=

## pg_hba.conf
TYPE   DATABASE USER  CIDR-ADDRESS  METHOD

## password file
host:port:dbname:user:password


# CMD
psql --version
cat $PGDATA/PG_VERSION
pg_controldata data_dir | grep "system identifier"
psql -l
createdb $DB

# SQL
select  version();
select date_trunc('second', current_timestamp - pg_postmaster_start_time()) as uptime;
select datname from pg_database;
CREATE DATABASE $DB;
