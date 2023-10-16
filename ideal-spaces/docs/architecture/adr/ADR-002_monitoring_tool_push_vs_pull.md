# Monitoring tool - push vs pull

## Context
Datadog has been proposed by ADEO/LMFR customer and Cyncly has separate PSR - Performance, Security and Reliability assessment ongoing task. Considering datadog as monitoring tool for infrastructure, application logs, tracing, etc. this could bring consistent experience to engineers and other end users. 

## Decision
Push based metrics collector such as datadog or similar could satisfy monitoring requirement as it tends to be easy setup compared with pull model (like prometheus) considering short live application complexity and relatively small size of logs, metrics, etc that generate.   

Having said that we would review our monitoring toolsets when we need to scale this requirement.

## Consequences
* There could be latency on push model when large amount of data are collected. 
* Due to latency, real-time monitoring experiences would be impacted.