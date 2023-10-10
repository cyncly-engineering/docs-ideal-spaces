# Observability/Monitoring tool - push vs pull

## Context
ADEO/LMFR customer has order UX monitoring requirement and Cyncly has separate PSR - Performance, Security and Reliability evaluation tasks. Considering datadog as monitoring tool for infrastructure, application logs, tracing, etc. this could bring consistent experience to engineers and other end users. 

## Decision
Push based metrics collector such as datadog or similar could satisfy monitoring requirement as it tends to be easy setup compared with pull model (like prometheus - considering short live application monitoring setup complexity with pushgateway server) and relatively small size of logs, metrics, etc which generated.   

Having said that we would review our monitoring toolsets when we need to scale monitoring requirements.

## Consequences
* There could be latency on push model when large amount of telemetry data are routing. 
* Due to latency, real-time monitoring experiences could be impacted and critical alerts can't be delivered in timely manner.