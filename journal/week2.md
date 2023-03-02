# Week 2 — Distributed Tracing

adding honey comb to backend 

OTEL_EXPORTER_OTLP_ENDPOINT: "https://api.honeycomb.io"
OTEL_EXPORTER_OTLP_HEADERS: "x-honeycomb-team=${HONEYCOMB_API_KEY}"
OTEL_SERVICE_NAME: "${HONEYCOMB_SERVICE_NAME}"


from opentelemetry import trace

tracer = trace.get_tracer("tracer.name.here")


Instrument our backend flask application to use Open Telemetry (OTEL) with Honeycomb.io as the provider
Run queries to explore traces within Honeycomb.io
Instrument AWS X-Ray into backend flask application
Configure and provision X-Ray daemon within docker-compose and send data back to X-Ray API
Observe X-Ray traces within the AWS Console
Integrate Rollbar for Error Logging
Trigger an error an observe an error with Rollbar
Install WatchTower and write a custom logger to send application log data to CloudWatch Log group




Instrument Honeycomb for the frontend-application to observe network latency between frontend and backend[HARD]
Add custom instrumentation to Honeycomb to add more attributes eg. UserId, Add a custom span
Run custom queries in Honeycomb and save them later eg. Latency by UserID, Recent Traces


export ROLLBAR_ACCESS_TOKEN="dfd6c6ceb95248abb0a71f5b77d500db"
gp env ROLLBAR_ACCESS_TOKEN="dfd6c6ceb95248abb0a71f5b77d500db"