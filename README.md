# bazadannix
PostgreSQL
sudo apt-get update
sudo apt-get install postgresql postgresql-contrib
postgres --version
psql postgres
\help
\help [имя команды]
createuser -P --interactive
CREATE ROLE имя_новой_роли WITH LOGIN CREATEDB CREATEROLE; // В конце обязательно ставим ;
\password имя_роли
DROP ROLE имя_роли;
drop user имя_роли
ALTER USER имя_роли WITH PASSWORD 'новый_пароль';
createdb bazadannix_БД
CREATE DATABASE bazadannix_БД;
drop database bazadannix_БД
DROP DATABASE bazadannix_БД;
psql
psql -d bazadannix_БД
psql -U имя_роли -h localhost -W
psql -U имя_роли -d имя_базы -h localhost -W // Разница в том, что явно указано название БД
pg_dump -h хост -U имя_роли -F формат_дампа -f путь_к_дампу имя_БД
pg_dump -h localhost -U mybase -F c -f /home/user/backups/dump.tar.gz mybase
pg_restore -h хост -U имя_роли -F формат_дампа -d имя_базы путь_к_дампу
