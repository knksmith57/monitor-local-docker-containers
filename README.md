# monitor local docker containers

> monitor docker containers on the current host using [Telegraf], store to [InfluxDB], and visualize with [Chronograf]

## quickstart

```sh
$ git clone https://github.com/knksmith57/monitor-local-docker-containers.git \
    && cd $_

$ docker-compose up -d

## open http://localhost:8888

## note: arbitrary DogStatsD ingestion is also supported on :8125/udp
$ echo -n "custom_metric:60|g|#shell:52" \
  | nc -4u -w0 localhost 8125
```

[telegraf]: https://www.influxdata.com/time-series-platform/telegraf/
[influxdb]: https://www.influxdata.com/time-series-platform/
[chronograf]: https://www.influxdata.com/time-series-platform/chronograf/
