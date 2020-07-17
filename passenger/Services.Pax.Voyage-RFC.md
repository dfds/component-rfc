# Services.Pax.Voyage RFC
## 1 Abstract
This document proposes a component for passenger voyages. 
The component exposes terminal locations and departure schedules for passenger routes.	

## 2 Status
Accepted

## 3 Component purpose
Provides general information on our passenger voyages allowing our customer XPs to present sailing schedules. Sends events about changes to departure schedules for other components to react upon.

## 4 Capability
### 4.1 Level 1 
Manage routes

## 5 API
### 5.1 Short API description
The API can be used to PUT departure schedules
The API can be used to GET departures, terminals and routes

### 5.2 Contract
http://api.dfds.cloud/prod/voyage/swagger/index.html

## 6 Events
### 6.1 Events published by the component
- *Departure Scheduled* - Raised when a new departure has been scheduled

- *Departure rescheduled* - Raised if the scheduled departure time changes

- *Arrival rescheduled* - Raised if the scheduled arrival time changes

- *Departure cancelled* - Raised the the sceduled departure is cancelled

## 7 Hosting
Hellman k8s cluster in AWS

## 8 Inner architecture
Service is event sourced using Marten with Postgresql as a backing store.
Events are published using outbox pattern.
