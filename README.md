# MUST READ!!!

Open and read the docs -> [Open Telemetry Protocol v1.37.0 Specification](https://github.com/open-telemetry/opentelemetry-specification/blob/v1.37.0/specification/protocol/exporter.md)

## OTLP Endpoint Configuration (All signal)
All signals are enabled by default, using single endpoint configuration automatically.
### `http/protobuf` (default)
```
OTEL_EXPORTER_OTLP_ENDPOINT=http://<http-endpoint>:4318
OTEL_EXPORTER_OTLP_TIMEOUT=10s
OTEL_EXPORTER_OTLP_PROTOCOL=http/protobuf
```
### `http/json`
```
OTEL_EXPORTER_OTLP_ENDPOINT=http://<http-endpoint>:4318
OTEL_EXPORTER_OTLP_TIMEOUT=10s
OTEL_EXPORTER_OTLP_PROTOCOL=http/json
```
### `grpc`
```
OTEL_EXPORTER_OTLP_ENDPOINT=http://<grpc-endpoint>:4317
OTEL_EXPORTER_OTLP_TIMEOUT=10s
OTEL_EXPORTER_OTLP_PROTOCOL=grpc
```

## OTLP Endpoint Configuration (Individual)

```
OTEL_EXPORTER_OTLP_TRACES_ENDPOINT=http://<endpoint>:4318/v1/traces
OTEL_EXPORTER_OTLP_METRICS_ENDPOINT=http://<endpoint>:4318/v1/metrics
OTEL_EXPORTER_OTLP_LOGS_ENDPOINT=http://<endpoint>:4318/v1/logs
OTEL_EXPORTER_OTLP_TIMEOUT=10s
OTEL_EXPORTER_OTLP_PROTOCOL=http/protobuf
```

## Disabling individual signal
```
OTEL_METRICS_EXPORTER=none
OTEL_TRACES_EXPORTER=none
OTEL_LOGS_EXPORTER=none
```

## Env vars
Open and read the docs -> [Open Telemetry SDK Environment Variables](https://opentelemetry.io/docs/specs/otel/configuration/sdk-environment-variables/)

```
OTEL_SERVICE_NAME=<service-name>
OTEL_RESOURCE_ATTRIBUTES=<key1>=<val1>,<key2>=<val2>
# log level default to info
OTEL_LOG_LEVEL=<log level>
```