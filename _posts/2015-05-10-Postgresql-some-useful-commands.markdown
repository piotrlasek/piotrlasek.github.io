---
layout: post
title: "Some usefule PostgreSQL commands"
date: 2015-05-10 12:00:00
categories: 
---

Backup database:

pg_dump db_name > db_name_dump.sql

scp user_name@192.168.56.101:db_name_dump.sql .

sudo -u postgres psql

create user user_name;

grant postgres to user_name;

create database slicer owner=user_name;

alter user postgres with password 'postgres';

\i db_name_dump.sql

\d


sudo -u postgres createdb -O piotr rm

Access from remote servers:

/etc/postgresql/9.3/main/postgresql.conf
listen_addresses = '*'

/etc/postgresql/9.3/main/pg_hba.conf
host    all             all             0.0.0.0/0            md5

sudo service postgresql restart



