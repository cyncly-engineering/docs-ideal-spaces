## Description
Focus on generation, collection, management and export of telemetry data such as traces, metrics, logs.

### Desire outcome or benefits
Create visualization out of telemetry data to meet monitoring ~~and observability~~ requirements on latency, traffic, errors and saturation.

### Business requirement

Analyzing long term trends
How big is my database and how fast is it growing? How quickly is my daily-active user count growing?

Comparing over time or experiment groups 
Are queries fast? How much better is my redis hit rate with an extra node? Is my site slower than it was last week?

alerting - something is broken, and somebody needs to fix it right now! Or, something might break soon, so somebody should look soon. 

A bashboards should answer basic questions about your service, and normally include some form of latency of success and latency of failed requests, traffic, errors, saturation 

Conducting ad hoc retrospective analysis(i.e., debugging)
Our latency just shot up; what else happened around the same time?

### In scope
Black-box monitoring - including UX monitoring
White-box monitoring 

### Preconditions

### Constrainsts

### Assumptions
Avoid any situation that requires someone to stare at a screen to watch for problems

### Reference 
[opentelemetry](https://opentelemetry.io/)
[application-insights](https://learn.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview?tabs=net#application-insights-overview)
https://sre.google/

### Business values
monitor key business and performance indicators? PO item 



