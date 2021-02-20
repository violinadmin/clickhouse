# clickhouse

docker-compose для поднятия двух инстансов clickhouse-server с асинхронной мастер-мастер репликацией и без авторизации. Один инстанс поднимается на 9000, другой на 9001.

Подключение для первого инастанса:

```
clickhouse-client
```

или

Для второго:

```
clickhouse-client --port 9001
```

Если на хосте нет clickhouse-client, то можно использовать client из контейнера:

```
docker run -it yandex/clickhouse-client --host ${serverip|hostip}
```