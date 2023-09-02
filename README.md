## sqlfdef

```sh
curl -OL https://github.com/k0kubun/sqldef/releases/download/v0.11.20/mysqldef_linux_amd64.tar.gz
tar xf mysqldef_linux_amd64.tar.gz -C /usr/local/bin/
```

```sh
docker compose exec database /usr/bin/mysqldump --user=wp_user --password=wp_password --no-tablespaces --no-data main > schema.sql
```
