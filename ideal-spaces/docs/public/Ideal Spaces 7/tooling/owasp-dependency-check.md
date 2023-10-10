# OWASP 

We monitor the libraries that our services use for potential known and published vulnerabilities. 

## Regular checks

### Report

### Failing pipeline

## Suppression

Our goal is to have no suppression without a good reason, and to detail those reasons.

If the pipeline reports a false positive, it needs to be suppressed by adding a suppression rule in `etc/owasp-security-checks/owasp-suppressions.xml`.
The HTML report contains buttons to generate the needed suppression rule.

### Timeouts 

We put all suppression on a timeout (e.g. three month) and review them after that. This also keeps the file from growing unlimited.
