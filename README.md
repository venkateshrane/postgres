# postgres
Related to Postgres

Check Locking in postgres DB
==============================
select pid,usename,pg_blocking_pids(pid) as blocked_by , query as blocked_query from pg_stat_activity where cardinality(pg_blocking_pids(pid)) > 0;

Terminate PG Session from database
==================================
select pg_terminate_backend(pid);
