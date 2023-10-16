# Ideal Spaces 6 postmortem(#incident [Bug 622695](https://dev.azure.com/2020Development/2020%20Programs/_workitems/edit/622695))

### Date : 2023-09-27

### Authors: Om, Pandurang, Siddhesh, Sagar, Sanketkumar, Benoit, Jestha

### Status
Complete, action items are in progress

### Summary


### Impact
Estimated x millions queries lost, $x revenue impact
* End user Impact
* Infrastructure impact
* Productivity impact 
### Root Causes
Cascading failure due to combination of profiler production IS 6 applications and exceptionally  CPU intensive catalog search failed operation triggered. Under normal circumstances, the rate of task failure due to catalog search failure is low enough to be unnoticed. 

### Trigger
PCS triggered CIC Decor cabinet catalogue by sudden increase CPU peak and combination of application insights profiler runs for 2 mins per every hour

### Resolution
Disabled profiler and deactivated CIC Decor Cabinet catalog to mitigate the cascading failure.

### Detection
Traces are investingate, found many HTTP requests execution time take over 40 mins and 3x slow TCP wait time 

Detected high level of HTTP 500x 

## Action Items
* Disabled profiler
* Deactivated CIC Decor Cabinates catalog
* Increase visibility
* Review scale out rule 
* Detect IP triggers CIC Decor Cabinet catalog
* Define SLO/SLI - identify catalog that bringing issue
* Review architecture - Workload distributed via CDN Frontdoor
* ~~Comms via MS Team and email~~
* Add Kusto query in workbook 
## Lessons Learned

### What went well

### What went wrong
~~No alerts or; alerts triggered but those information are lost due to noise~~
~~Failure of anomalies detection~~
High discovery time
Application failure of fail fast and safely

### Where we got lucky

## Timeline
2023-09-21 (**all times in UTC**)

* 2023-09-15 13:32 Enabled application insights profiler
* 2023-09-15 ??:?? **OUTAGE BEGINS** Loading catalogs information and search backends start metling down under load
* 2023-09-19 08:37 **INCIDENT BEGINS** [Bug 622695](https://dev.azure.com/2020Development/2020%20Programs/_workitems/edit/622695) incident reported by customer support team.
* 2023-09-20 ??:?? Disabled application insights profiler for product offering
* 2023-09-22 06:07 **OUTAGE MITIGATED** Deactivated CIC Decor Cabinets catalog 
* ??:?? ~~HTTP errors rates remain within SLO?~~ No task failure observed 
* ??:?? **INCIDENT ENDS** reached average CPU 60% and maximum CPU 95% with nominal performance 
* ??:?? **OUTAGE ENDS** all upstream requests are responsed in milliseconds 
* 2023-09-25 10:46 ~~Jestha wrote email to Joris CSM~~ **INCIDENT ENDS** Confirmed IS 6 application performance is back to normal

## Supporting information