# Document.DataExtraction RFC
## 1 Abstract
This document proposes a component that will handle data extraction from documents by sending them to a 3rd-party service for processing and receive the output and send it out to the requesting component.

## 2 Status
Open

## 3 Component purpose
Manage interactions with the 3rd-party data extractor service. This component is meant to be generic so that it can be called by any other component inside our K8s cluster.
The other components that call this service and request a data extraction job by supplying a file and the method of extraction.
The data extraction job status can be queried, while the result of the extraction is sent out to the caller component that requested the job.

## 4 Capability
Document-DataExtraction

## 5 API
### 5.1 Short API description
The API can be used to POST a data extraction request

### 5.2 Contract
https://app.swaggerhub.com/apis/CraleDFDS/DataExtraction/1.0.0

## 6 Events
### 6.1 Events published by the component
The component publishes events regarding job status updates and data extraction results

- *DocumentReceivedForDataExtraction* - Raised when a focument is received for data extraction

- *DataExtractionStarted* - Raised when a data extraction job is started

- *DataExtractionInvalidated* - Raised when a data extraction job is was marked as invalid

- *DataExtractionValidated* - Raised when a data extraction job is was marked as valid

- *DataExtractionCompleted* - Raised when a data extraction job is completed, contains the result of the extraction

### 6.2 Events subscribed to by the component
TBD

## 7 Hosting
Hellman k8s cluster in AWS

## 8 Inner architecture
Events are published to Kafka  
PostgreSQL DB for outbox  
Security for communication directly to this service (fx BFF's) will be OAuth
