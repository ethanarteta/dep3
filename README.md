<p align="center">
<img src="https://github.com/kura-labs-org/kuralabs_deployment_1/blob/main/Kuralogo.png">
</p>
<h1 align="center">C4_deployment-3.1<h1> 

The Story
-----------------------------------------
We’re a tech start-up company with a URL shortener tool. We have a SLA with Nike to provide them access to our URL shortener. In the SLA, we are only allowed 20 minutes of downtime a year. If anything happens to the URL shortener, we must communicate any incidents to Nike.
 
Scenario
-----------------------------------------
A new hire was tasked with updating the URL shortener. The new hire committed version 2 of the application to the main branch. Which automatically triggered a build, test, and deploy to the production server, replacing version 1 of the application running on the server.


- Follow the in-class instructions
  
# Post-Incident Report

## Incident Summary

### Reason for the Incident

This incident occured due to an error in the "application.py" file where a change was made: by changing "json.load" to "json.loads" this caused an internal server error to occur. This disruption resulted in unexpected downtime of our service to Nike.

### Duration of Downtime

The downtime lasted for approximately 6 minutes as the version 2 of the application was rolled back to the stable state of version 1 and then redeployed. The downtime of the application is within the 20 minutes of downtime allowed within our SLA agreeement.

## Steps Taken to Resolve the Incident

1. **Immediate Response:** As soon as the incident was detected, our team was given 15 minutes to find a solution to the incident.

2. **Isolation:** The first step was to isolate the new deployment and roll back to the previous version (version 1) of the URL shortener application. This was done to mitigate further disruptions and restore service stability.

3. **Investigation:** A thorough investigation was conducted to identify the root cause of the incident. It was determined that the disruption was caused by a misconfiguration in the deployment process, specifically in the python code concerning "json.load".

4. **Resolution:** Once the root cause was identified, the misconfiguration was corrected, and the deployment of version 2 was redeployed. This time, it was successful without causing any further disruptions.

## Incident Resolution

The incident was eventually fully resolved after the successful deployment of version 2 of the application with the corrected configuration. The service has been restored to its normal operational state, and there have been no subsequent disruptions.

## Preventative Measures

To prevent a similar incident from happening in the future and to ensure we meet our SLA commitments:

1. **Improved Deployment Process:** We will review and enhance our deployment process to include stricter validation checks and a private testing environment to test the web server before deployment. This will reduce the risk of misconfigurations causing downtime.

2. **Enhanced Monitoring:** We will implement enhanced monitoring and alerting systems that can quickly detect any anomalies during deployment or application performance (Datadog). This will allow us to respond proactively to potential issues before they result in downtime.

3. **Training and Documentation:** We will provide additional training to our development and operations teams on best practices for deployment and configuration management. Clear documentation will also be made available to ensure everyone is aligned on deployment procedures.
