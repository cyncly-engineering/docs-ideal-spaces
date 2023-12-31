# Datadog in LMFR prod

## Important links 

1. [LMFR Dashbroad](https://p.datadoghq.eu/sb/aee7596e-6682-11ee-a351-da7ad0900005-7a2d23d23a6dab9beb8fd8833e071f33)

<iframe width="100%" height="450" name="LMFR Dashboard" src="https://p.datadoghq.eu/sb/aee7596e-6682-11ee-a351-da7ad0900005-7a2d23d23a6dab9beb8fd8833e071f33"></iframe>

1. [LMFR traces](https://app.datadoghq.eu/apm/traces)
1. [Logs]()
1. [Logs error outlier](https://app.datadoghq.eu/watchdog/outlier/3bb742d3-8214-37bb-9110-9f2ad02474f9)
1. [Monitoring](https://app.datadoghq.eu/monitors/manage?q=env%3Aprod&order=desc)
1. [Application security](https://app.datadoghq.eu/security/appsec)

## Upcoming tasks

1. Alerting on what matters
    a. send alert when a particular issue occured x times in a specific timeframe.
    
1. Investigating performance issues 
1. Scaling events & alerts 

## Available features in Datadog platform
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

    a. Custom metrics ![](https://geps.dev/progress/0)

1. Logs ingestion ![](https://geps.dev/progress/100)

    a. Rentention policy ![](https://geps.dev/progress/0)
    
    b. Archived policy ![](https://geps.dev/progress/0)

    c. Rotation policy ![](https://geps.dev/progress/0)

1. APM ![](https://geps.dev/progress/100) 

    a. Connect traces with RUM ![](https://geps.dev/progress/0)

    b. Connect traces with logs ![](https://geps.dev/progress/100)

1. UX Monitoring 

    a. Real User Monitoring ![](https://geps.dev/progress/0)
    
    b. API Synthetic Monitoring ![](https://geps.dev/progress/30)
    
    c. Browser Synthetic Monitoring ![](https://geps.dev/progress/100) 

1. Security 
    
    a. Application security ![](https://geps.dev/progress/50)
    
    b. Cloud SIEM ![](https://geps.dev/progress/0)

1. SLIs/SLOs 

    a. Uptime/online monitoring ![](https://geps.dev/progress/50) 
    
    b. Availability/Counter metrics based SLOs ![](https://geps.dev/progress/70)
    
    c. Latency/Monitoring based SLOs ![](https://geps.dev/progress/100)

1. Dashboards ![](https://geps.dev/progress/100)

    a. Organizational overview ![](https://geps.dev/progress/0)

    b. LMFR prod dashboard ![](https://geps.dev/progress/100)

1. Monitoring ![](https://geps.dev/progress/100)

    a. Watchdog ![](https://geps.dev/progress/0)
    
    b. Anomaly detection ![](https://geps.dev/progress/100) 
    
    For example: 
    service response rate 100% 5xx errors - this might indicates that the service is offline.
    should send a notification
    
    c. Metrics forecast ![](https://geps.dev/progress/0)
    
    d. Outlier detection ![](https://geps.dev/progress/100)

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

    b. Org/Datadog tag policy ![](https://geps.dev/progress/0)

## Resources

Gabriel, Robert, Pandurang, Siddhesh, Jestha

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

## Status of features available 

[IS 7 map](https://cyncly-my.sharepoint.com/:x:/p/jestha_wangkheirakpam/EXf-lPd4HaBPurHrHs_KJ9EBwo0NWDM38lS-HkV2UT90JA?e=V9wYrC)

<iframe width="100%" height="150" name="status" src="https://cyncly-my.sharepoint.com/:x:/p/jestha_wangkheirakpam/EXf-lPd4HaBPurHrHs_KJ9EBwo0NWDM38lS-HkV2UT90JA?e=V9wYrC"></iframe>