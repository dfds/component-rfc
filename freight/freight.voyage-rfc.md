# Freight.Voyage RFC
## 1 Abstract
This document proposes a component for freight voyages. The component exposes departures for freight routes including checkin status for channel voyages.

## 2 Status
accepted

## 3 Component purpose
Provides general information on our freight voyages. Sends events about changes to departure schedules and statuses (check-in status for channel/tallied) for other components to react upon.

## 4 Capability
### 4.1 Level 1
N/A

## 5 API
### 5.1 Short API description
The API can be used to GET freight departures with check-in status, voyage status (tallied) and times availble for bookings.

### 5.2 Contract
https://voyage-component.freight.dfds.cloud/swagger/index.html

## 6 Events
### 6.1 Events published by the component
- *Voyage Created* - Raised when a new departure has been scheduled.

- *Voyage Updated* - Summary event, raised if anything is updated on the departure.

- *Voyage Cancelled* - Raised when a departure is cancelled.

### 6.2 Events subscribed to by the component
- *Vessel Events* - Used to translate the imo number to the vessel Id from MVS component

- *Route Events* - Used to translate the Port of loading/Port of discharge to a Route Id from Route Component

- *Legacy voyage events from Phoenix* - Source of truth until strangulation is complete.


## 7 Hosting
Hosted in Fargate, Phoenix freight AWS account

## 8 Inner architecture
Domain events are sourced in a DynamoDb table
Events are published to a AWS topic in the same account
