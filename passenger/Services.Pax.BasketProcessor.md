# Services.Pax.Basket RFC
## 1 Abstract
This document proposes a component that will handle passenger bookings in a basket.

## 2 Status
Open

## 3 Component purpose
Keeps track of a customer's booking and it's content, such as departures, passengers, vehicles.  
A basket lives in the component until it has been payed for or times out.

## 4 Capability
### 4.1 Level 1
Package-Holidays

## 5 API
### 5.1 Short API description
The API can be used to POST a basket when initiating a booking  
The API can be used to PUT a basket for updating it's content  
The API can be used to GET a basket and it's content 

### 5.2 Contract
Not yet available

## 6 Events
### 6.1 Events published by the component
TBD

- *BasketDepartureAdded* - Raised when a departure has been added to a basket

- *BasketCustomerAdded* - Rasised when a customer (lead passenger) has been added to a basket

- *TermsAndConditionsAccepted* - Raised when the customer has accepted the terms and conditions as part of confirming the basket

### 6.2 Events subscribed to by the component
TBD

- *BasketReservationCreated* - Used to validate that a reservation could be created from the basket's content

- *BasketReservationCreatedFailed* - Used to know that a reservation could not be created

## 7 Hosting
Hellman k8s cluster in AWS

## 8 Inner architecture
Events are published to Kafka  
DynamoDB  
Security for communication directly to this service (fx BFF's) will be OAuth