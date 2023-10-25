# Enhance Datadog POC

## Success Criteria

## Estimate duration and effort

## Scope of POC 
1. Integration

    a. Azure DevOps ![](https://geps.dev/progress/100)

    c. MS Team ![](https://geps.dev/progress/100)

    Datadog Connector is added in MS Team

    d. SSO with SAML ![](https://geps.dev/progress/0)

1. Infrastructure

    a. Azure severless ![](https://geps.dev/progress/100)

    b. Agent ![](https://geps.dev/progress/100)

    c. Univeral service monitoring ![](https://geps.dev/progress/0)

1. Metrics ![](https://geps.dev/progress/100)

    a. Custom metrics ![](https://geps.dev/progress/100)

1. Logs ingestion ![](https://geps.dev/progress/100)

    a. Rentention policy ![](https://geps.dev/progress/0)
    
    b. Archived policy ![](https://geps.dev/progress/0)

    c. Rotation policy ![](https://geps.dev/progress/0)

1. APM ![](https://geps.dev/progress/100) 

    a. Connect traces with RUM ![](https://geps.dev/progress/100)

    b. Connect traces with logs ![](https://geps.dev/progress/100)

1. UX Monitoring 

    a. Real User Monitoring ![](https://geps.dev/progress/100)
    
    b. API Synthetic Monitoring ![](https://geps.dev/progress/0)
    
    c. Browser Synthetic Monitoring ![](https://geps.dev/progress/0) 

1. Security 
    
    a. Application security ![](https://geps.dev/progress/100)
    
    b. Cloud SIEM ![](https://geps.dev/progress/0)

1. SLIs/SLOs 

    a. Uptime monitoring ![](https://geps.dev/progress/50) 
    
    b. Metrics based SLOs ![](https://geps.dev/progress/100)
    
    c. Monitoring based SLOs ![](https://geps.dev/progress/50)

1. Dashboards ![](https://geps.dev/progress/100)

    a. Organizational overview ![](https://geps.dev/progress/0)

    b. Product/service dashboard ![](https://geps.dev/progress/100)

1. Monitoring ![](https://geps.dev/progress/100)

    a. Watchdog ![](https://geps.dev/progress/0)
    
    b. Anomaly detection ![](https://geps.dev/progress/50) 
    
    For example: 
    service response rate 100% 5xx errors - this might indicates that the service is offline.
    should send a notification
    
    c. Metrics forecast ![](https://geps.dev/progress/0)
    
    d. Outlier detection ![](https://geps.dev/progress/0)

    e. Forecast monitoring ![](https://geps.dev/progress/50) 
    
    For example: 
    requests rate >= 20; should get alerts 
    or; logs filling up fast, alert a week before for rotation policy 
    or; forecast biz KPIs

    f. Manage downtime ![](https://geps.dev/progress/0)

1. Working with incident - declare incident, publish postmortem ![](https://geps.dev/progress/0)

1. Dora metric reporting ![](https://geps.dev/progress/0)

1. Best practises

    a. Tagging resources ![](https://geps.dev/progress/100)

    b. Org/Datadog tag policy ![](https://geps.dev/progress/50)

## Resources

Gabriel, Pandurang, Siddhesh, Jestha

## Service Availability Definitions

In Order to calculate the availability of the service, three indicators are taken into account.

1. The service is available.
2. The service is online.
3. The service response time is under the defined latency

This indicators will consider the following major features/functions:

1. Login
2. Creation of a design/project
3. Search for a design/project
4. Load a design/project
5. Save a design/project
6. Display pricing
7. Retrieve item list for design/project

**Indicator 1 - Availability Calculation** = SR1 / TR1 for each major function listed above 

SR1 = Total # of Requests in the Reporting Period with an http response code below 500

TR1 = Total # of Requests in Reporting Period

**Indicator 2 - Online Calculation** = SR2 / TR2 for synthetic requests to be defined(see section Yearly review)

SR2 = Total # of Requests in Reporting Period with an http response code below 400

TR2 = Total # of Requests in Reporting Period

**Indicator 3 - Latency** The latency calculation is to be defined(see section Yearly review)

**Overall Service Availability Calculation** = For a given period of time, the Service availability will always be the lowest availability of the three indicators above.