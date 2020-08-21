# Freight.Schedule RFC
## 1 Abstract
This document proposes a component for freight schedules. The component exposes schedule information for freight routes.

## 2 Status
accepted

## 3 Component purpose
Provides general information on our freight schedule.

## 4 Capability
### 4.1 Level 1
Shows schedule information including the port of loading, port of discharge, status, transport type (Limited to voyage), Scheduled times and actual times of arrival and departure.

## 5 API
### 5.1 Short API description
The API can be used to GET freight schedule with a date range, port of loading and port of discharge.

### 5.2 Contract
https://schedule-component.freight.dfds.cloud/swagger/index.html

## 6 Events
### 6.1 Events published by the component
Currently no events raised.

### 6.2 Events subscribed to by the component

- *Route Events* - Used to validate the route on the schedule.

- *Voyage Events* - Used to get the voyage information to populate the schedule.

## 7 Hosting
Hosted in Fargate, Phoenix freight AWS account

## 8 Inner architecture
	Aurora MySQL Database
