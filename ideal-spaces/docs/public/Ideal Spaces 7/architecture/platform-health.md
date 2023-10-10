Title: Platform Health

# Platform Health

## Objective

Provide visibility of planned work that Ideal Space 7 team need to do (and are already doing) in order to keep our platforms running and meet our (contractual and moral) obligations to the business, our users and customers.

## Key result

Teams include this type of work on documents in a way that can be discussed, understood and effectively prioritised as an integral part of work in our focus areas.

## Categories

### Buildable

* It can be built via a build triggered by Git commits on a supported CI platform (generally Azure pipeline)
    * This will need to be checked regularly, as environmental changes (including external) can alter this at any time
* It can be built in a reproducible manner (considering Docker Compose or Docker could be better option)
* The build will test and report on constraints (e.g. it’ll tell you if you are trying to build it with the wrong version of .NET framework)
* Where practical, the build can be run locally (without Docker) if the dependencies exist - this is to make development more convenient, but may be challenging or even impossible for applications with complex dependencies
* It should be buildable via a script called 'build' (or 'do-build' where build is blocked by framework, e.g. React)
* Upstream applications should provide a known QA environment which can be used by dependants for testing

### Deployable

* It can be deployed to a supported environment (e.g. Azure app service)
    * This will need to be checked regularly, as environmental changes (including external) can alter this at any time
* The deployment is done automatically after the CI build passes
* Smoke testing is in place to ensure the deployment is working
* [Consumer-Driven Contracts (CDC)](https://martinfowler.com/articles/consumerDrivenContracts.html) are in place to test that dependencies are compatible
* No manual action is required during the deployment, i.e. the deployment should not be gated
* The application can be terminated or suspended on demand in case of critical issues (e.g. data leaks)
    * E.g. a `az webapp stop` is fine, as long as it leaves the system in a safe, restartable state (e.g. no data corruption is caused by the shutdown method)
    * This may require documentation where a service cannot simply be stopped safely
    * Where users need to be informed that this page/service is currently not available, it might be necessary to have a maintenance page application at hand which then is deployed on the route(s) of the stopped application.

### Secure

* Dependencies are kept up to date
* Automatic scanning is in place (e.g. Contrast, GitHub dependency checks, Snyk, …)
* Any known exploitable issues are resolved as a matter of urgency


### Performant

* It has defined objectives for performance - this is particularly critical where there are clients of this application with their own objectives
* The performance is monitored and significant changes are corrected

### Scalable

* The applications scale to meet the capacity requirements forecast for the medium-term

### Observable

* Critical metrics are captured for the application via the supported monitoring platforms
    * The nature of these metrics will depend on the application
    * Alongside runtime metrics these may also include code and other non-functional metrics that contribute to maintaining and supporting the application
* Error information is captured via supported tools (e.g. ApplicationInsights, datadog, Sentry, etc.)

### Accessible

* It meets all contractual and legal requirements for accessibility

### Browser Compatibility

* It is compatible with our currently supported set of browsers
* It is adapted for upcoming changes to supported browsers (e.g. Chrome cookie changes)

### Dependencies

* All dependencies are supported versions and have no known security vulnerabilities
* Where a dependency is no longer supported mitigations are made (e.g. a branch that we can support) or a migration to a supported alternative is completed

### Understandable

* The purpose of applications should be clear, as should the user/business problems it solves
* It should be possible for a developer to understand the basics of how an application is built and works without requiring a chat with anyone

### Lifecycle

* An application should have a technical and product owner within Cyncly - including if the app is in C&M or supported by a third party - and this must be documented in the repository's README file
* If the ownership of the application changes then a handover process must take place, transferring all required knowledge to maintain the application, and the change in ownership must be broadcast to all stakeholders
* Applications at the end of their useful life should have a sunsetting process defined, including communication to all potential users and a termination date
