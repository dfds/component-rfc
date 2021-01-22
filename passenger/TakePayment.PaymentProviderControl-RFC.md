# TakePayment.PaymentProviderControl RFC
## 1 Abstract
This document proposes a component that will handle control between a frontend and a payment provider.
It will be responsible for communication from the frontend-code to setup and provide necessary information to the payment provider so that the frontend can show a payment popup and take payment from the customer.

## 2 Status
Suggested

## 3 Component purpose
We will aim to make it as generic as possible.

## 4 Capability
### 4.1 Level 1
Take Payment

## 5 API
### 5.1 Short API description
By providing a tenant/merchant it will be configure "next step" for the payment provider after taking payment.

### 5.2 Contract

## 6 Events
### 6.1 Events published by the component
No planned events ATM

## 7 Hosting
Hellman k8s cluster in AWS

## 8 Inner architecture
It will be a NodeJS application without subscriber, dispatcher or database.