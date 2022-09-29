# ParthSekar.github.io


```mermaid
sequenceDiagram
Int Test->>+Azure Service Bus: Configures ReceiveEndpoint for CreateFileRequestResolved
Int Test->>+Azure Service Bus: Publishes CreateFileRequestSent
File Storage Service-->>+Azure Service Bus: 
Azure Service Bus->>+File Storage Service: Consumes CreateFileRequestSent 
File Storage Service->>+Azure Service Bus: Publishes CreateFileRequestResolved event 
Int Test->>+Azure Service Bus: Consumes CreateFileRequestResolved 
```
