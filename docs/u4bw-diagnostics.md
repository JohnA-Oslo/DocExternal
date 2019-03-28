# Unit4 Business World diagnostics

The log system in Unit4 Business World can be used to investigate issues experienced by users. In the context of Wanda, the Public Web API logs and the SOAP services logs are relevant. For details on how to configure logging see the Unit4 Business World technical guidelines.

This can be used to verify situations where a user does not have access to required public APIs, objects or SOAP service. In addition it can reveal other situation regarding missing configuration etc.

## Standard issues

1. User is not properly mapped in **User master file**. The associated **unit4_id** claim provided by Unit4 Identity Services must be mapped for a user to be able to call any web services.
2. User does not have access to the web service (endpoint). 
