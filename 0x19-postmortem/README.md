Task 0x19. Postmortem

Issue Summary:
Duration: 2/05/2024 From 06:00 PM until 07:30 PM.
Impact: The web page was down, resulting in service unavailability for almost all users with 98% who were affected.
Root Cause: There wewe a misconfiguration in the service then the system encountered errors when handling a high volume of requests, resulting in service degradation and eventual downtime.

Timeline:
6:00 PM: Initial users report of service unavailability.
6:15 PM: System monitoring alert indicate high database query response times.
6:20 PM: Software engineers were alerted and initiated an investigation
6:50 PM: They identified the failure in the system
7:15 PM: They made several attempts to restore service again.
7:30PM: The Service were restored and everything was normal.


Root cause:
This misconfiguration due to the change in API caused an error loop in the application code, leading to errors when handling a high volume of requests, resulting in service degradation and eventual downtime.

Then the issue was solved by terminating all existing connections and implementing connection pooling to manage resources efficiently and deploying similar issues.

Corrective and preventative measures:
To prevent similar incidents in the future, we have implemented the following:
Improve configuration management processes to avoid misconfigurations
Enhanced monitoring and alerting systems to detect abnormal system behavior.
Strengthened incident response procedures and communication channels
	
