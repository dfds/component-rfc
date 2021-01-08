# Services.Pax.CustomerCommunication RFC
## 1 Abstract
This document proposes a component that will handle the different types of communication that can take place between Seabook and a customer. The initial version will handle communication using the Iterable API which is currently used in Seabook to send out itinerary e-mails.
Furture communication types could include direct e-mail, SMS or SoMe.

## 2 Status
Suggested

## 3 Component purpose
Specialized in interaction with the Iterable API. The component will also own the relation between sales owners and Iterable campaigns/templates.

## 4 Capability
### 4.1 Level 1
Manage customers

## 5 API
### 5.1 Short API description
The API can be used to GET an outstanding payment URL for a reservation.

### 5.2 Contract
https://api.hellman.oxygen.dfds.cloud/prod/customercommunication/swagger/index.html

## 6 Events
### 6.1 Events published by the component
No planned events ATM

## 7 Hosting
Hellman k8s cluster in AWS

## 8 Inner architecture
Initial version will consist of a NServiceBus message subscriber and a Postgres DB.
