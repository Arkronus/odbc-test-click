# Инструкция

1. Установите драйвер для нужной операционной системы:

**Windows** <https://github.com/yandex/clickhouse-odbc/releases>

2. Установить сертификат

```bash
mkdir -p ~/.clickhouse-client /usr/local/share/ca-certificates/Yandex && \
wget "https://storage.yandexcloud.net/cloud-certs/CA.pem" -O /usr/local/share/ca-certificates/Yandex/YandexInternalRootCA.crt && \
wget "https://storage.yandexcloud.net/mdb/clickhouse-client.conf.example" -O ~/.clickhouse-client/config.xml
```

1. Установите драйвер clickhouse-odbc и укажите его настройки в файле odbc.ini:

```
Driver = path_to_driver
Description = ClickHouse driver
URL = <https://user1>:<password>@rc1a-mj1otp3ml6o6jva6.mdb.yandexcloud.net:8443/query
Database = db1
```