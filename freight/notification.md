# Notification RFC
## 1 Abstract
This document proposes a component for notifications. Primarily used for sending emails.

## 2 Status
accepted

## 3 Component purpose
Provides an abstraction of using iterable as our platform for sending emails. If we change from using iterable, in the future, we only have to change one component.

## 4 Capability
### 4.1 Level 1
N/A

## 5 API
### 5.1 Short API description
There is the ability to setup notification types (where you can set the iterable id to a freindly name, and supply API key). Also the ability to send a notification using that type.

### 5.2 Contract
https://notification-component-test.freight.np.dfds.cloud/swagger/index.html (Test - not yet in UAT/Prod)

## 6 Events
### 6.1 Events published by the component
N/A

### 6.2 Events subscribed to by the component
N/A

## 7 Hosting
Hosted in Fargate, Phoenix freight AWS account

## 8 Inner architecture
Secured with OAuth2 client credentials currently using AWS Cognito
