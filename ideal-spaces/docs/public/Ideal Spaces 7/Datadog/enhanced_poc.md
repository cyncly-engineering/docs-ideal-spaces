~~ADEO contract for IS 7~~

## Service Availability Definitions

In Order to calculate the availability of the service, three indicators are taken into account.

1. Login
2. Creation of a design/project
3. Search for a design/project
4. Load a design/project
5. Save a design/project
6. Display pricing
7. Retrieve item list for design/project

**Indicato 1 - Availability Calculation** = SR1 / TR1 for each major function listed above 
SR1 = Total # of Requests in the Reporting Period with an http response code below 500
TR1 = Total # of Requests in Reporting Period

**Indicator 2 - Online Calculation** = SR2 / TR2 for synthetic requests to be defined(see section Yearly review)
SR2 = Total # of Requests in Reporting Period with an http response code below 400
TR2 = Total # of Requests in Reporting Period

**Indicator 3 - Latency** The latency calculation is to be defined(see section Yearly review)

**Overall Service Availability Calculation** = FOr a given period of time, the Service availability will always be the lowest availability of the three indicators above.