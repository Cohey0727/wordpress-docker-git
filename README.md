# Wordpress with docker and git

Wordpress を Docker と Git を用いて開発しやすくすることを試す

## Install sqlfdef

### Mac

```sh
brew install sqldef/sqldef/mysqldef
```

### Linux

```sh
curl -OL https://github.com/k0kubun/sqldef/releases/download/v0.16.5/ssqldef_linux_arm64.tar.gz
tar xf ssqldef_linux_arm64.tar.gz -C /usr/local/bin/
```

## Database Dump

```sh
# with mysqldef
mysqldef -h docker.for.mac.localhost -P 43306 -u wp_user -p wp_password main --export > schema.sql

# with mysqldump
docker compose exec database /usr/bin/mysqldump --user=wp_user --password=wp_password --no-tablespaces --no-data main > schema.sql
```
