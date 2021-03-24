# INTEGRATION FROM AGILE TO WORKFRONT

## Overview

This repo includes services for integrating Project and Product data from Agile PLM to the Workfront application.

## High Level Architecture

Below picture depicts high level data flow. The design includes Workfront and Agile integration through EAI which is a cloud run service.
Expected response times have also been mentioned.

￼
## Workfront(WF) 
Workfront Fusion facilitates the development of automated functionality for Software as a service (SaaS) applications. Request is initiated by the WF UI and the WFF sends the request to EAI
 

## Enterprise Application Integration (EAI) 
Service is GCP CloudRun service which is invoked by Workfront Fusion (WFF). This receives the parameters in the get request headers and invokes a stored procedure function of Agile DB . Response from Agile will be sent back with headers and a body.


## Agile
In this context, a stored procedure function will be called by EAI and agile would execute the SP and send back the result to EAI.


## Service Details

1. [EAI]() 
