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
