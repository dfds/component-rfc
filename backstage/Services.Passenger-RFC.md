# Services.Passenger RFC
## 1 Abstract
This document proposes a component that will handle and store passengers. The component will expose an API for adding and handling passengers.

## 2 Status
Suggested

## 3 Component purpose
The component will store passenger information for all departures

## 4 Capability
### 4.1 Level 1
Manage customers

## 5 API
### 5.1 Short API description
The API can be used to PUT passengers for a specific booking number.
The API can be used to GET passengers for a specific booking number anonymised or not.
The API can be used to DELETE passengers given a passengerId.
The API can be used to DELETE all passengers on a booking given a booking number.
The API can be used to PUT passenger validation data for a specific booking number.

### 5.2 Contract
https://dfds.sharepoint.com/sites/ITDigitalPassengerTribe/Shared%20Documents/General/Passenger%20Experience/UK%20API/PassengerAPI.yml

## 6 Events
### 6.1 Events published by the component
No planned events ATM

## 7 Hosting
Hellman k8s cluster in AWS

## 8 Inner architecture
Initial version will consist of a Postgres DB. The API will assign clients roles with OAuth to specifiy request origin.