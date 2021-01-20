# Services.Pax.Basket RFC
## 1 Abstract
This document proposes a component that will handle passenger bookings as baskets.

## 2 Status
Open

## 3 Component purpose
Keeps track of a customer's booking and it's content, such as departures, passengers, vehicles. 
A basket lives in the component until it has been payed for or times out.

## 4 Capability
### 4.1 Level 1
PassengerBooking

## 5 API
### 5.1 Short API description
The API can be used to POST a basket when initiating a booking
The API can be used to PUT a basket for updating it's content
The API can be used to GET a basket (including basket status and content)

### 5.2 Contract
https://dfds.sharepoint.com/sites/ITDigitalPassengerTribe/Shared%20Documents/General/Trojans/Project%20documents/New%20Booking%20Experience%202021/services.pax.basket.yml

## 6 Events
### 6.1 Events published by the component
TBD

- *DepartureAddedToBasket* - Raised when a departure has been added to a basket

- *TermsAndConditionsAccepted* - Raised when the customer has accepted the terms and conditions as part of confirming the basket

### 6.2 Events subscribed to by the component
TBD

- *BookingCreated* - Used to validate that a booking could be created from the basket's content

## 7 Hosting
Hellman k8s cluster in AWS

## 8 Inner architecture
Events are published to ?
Aurora MySQL Database ?