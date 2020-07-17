# component-rfc
A component RFC is a lightweight way for development teams to get early feedback on component design from other development teams in all DFDS tribes.
It can also help other teams to get an overview of what is currently in the pipeline and help identify possiblities for component reuse across DFDS.

A component RFC is not meant to a roadblock for development. Teams should post RFC's as soon as they start thinking about creating a new component, but the team is free to start development, regardles of the the RFC status. They do not have to wait for the RFC to be reviewed or accepted.

## RFC Content
A component RFC consists of mandatory and optional content:
### {Service name} RFC
*Mandatory*

### 1 Abstract
*Mandatory*
Short description of the document.
This document proposes a component for ...

### 2 Status
*Mandatory*
Current status of the RFC
draft/open/accepted/rejected/superseded

### 3 Component purpose
*Mandatory*
Describes the purpose of the proposed component. What's the reason for exisitence, what functionality will be encapsulated in the component?

### 4 Capability
#### 4.1 Level 1 
*Mandatory*
Which capability does the proposed component belong to (e.g. TakePayment) 

#### 4.2 Level 2
*Optional*
If the component supports only a sub-capability, it can be listed here.

### 5 API
#### 5.1 Short API description
*Mandatory*
Short description of the API that the component will expose. Who's the intended users of the API, what are the primary features of the API

#### 5.2 Contract
*Optional*
Link to an OpenAPI specification of the API, if available at this stage.

### 6 Events
#### 6.1 Events published by the component
*Mandatory*
Short description of the domain events published by the component

#### 6.2 Events subscribed to by the component
*Optional*
If the component subscribes to events from other components, these can be listed here.

### 7 Hosting
*Optional*
If there's special things to note around hosting, it can be described here.

### 8 Inner architecture
*Optional*
In case the team wants to get feedback on the intended inner architecture of a component, this can be described here.


## Further reading
Here’s a bit of inspiration from Uber:
Starting a New Service
In a rapidly growing engineering organization, it can be difficult to keep track of all the efforts underway. This kind of growth demands a process to prevent duplicating work across teams. At Uber, we have solved this problem by requiring that authors of new services submit a Request for Comments (RFC), a high-level proposal of the new service that outlines its purpose, architecture, dependencies, and other implementation details for the rest of Uber Engineering to discuss. The RFC serves two purposes: 1) to solicit feedback for improving the service’s quality as it’s developed and 2) to prevent duplicate efforts or expose opportunities for collaboration.
https://eng.uber.com/building-tincup/
