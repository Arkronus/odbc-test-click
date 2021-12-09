# Инструкция

1. Установите драйвер для нужной операционной системы:

**Windows** <https://github.com/yandex/clickhouse-odbc/releases>

2. Установить сертификат

```bash
bash getcert.sh
```

1. Установите драйвер clickhouse-odbc и укажите его настройки в файле odbc.ini:

```
Driver = /opt/tableau/tableau_driver/clik/libclickhouseodbcw.so
Description = ClickHouse driver
URL = <https://user1>:<password>@rc1a-mj1otp3ml6o6jva6.mdb.yandexcloud.net:8443/query
Database = db1
```