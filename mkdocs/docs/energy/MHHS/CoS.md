# MHHS
The UK energy industry contains several essential roles and functions which must be undertaken in order for the regulated market of electricity supply and demand to work effectively.  
Market wide half-hourly settlement (MHHS) is an industry initiative to allow:  
- the circa. 32 million smart meters to provide faster data integration with energy market participants and settlement IT systems  
- simplification of interfaces and communications between market participants  

## Change of Supplier (CoS)
Where a customer (retail or business), for economic or service reasons, wants to move to another electricity supplier.  In this case, their metering operations must be closed down at one supplier and opened at a new supplier.   

```mermaid
sequenceDiagram
    autonumber
    participant Old Supplier
    participant New Supplier
    Participant CSS
    Participant Registration Service
    activate New Supplier
    New Supplier ->> CSS: switch request
    deactivate New Supplier
    activate CSS
    CSS->>Registration Service: notify
    activate Registration Service
    CSS-->>Old Supplier: de-activate
    CSS-->>New Supplier: activate (48hrs)
    deactivate CSS
    Registration Service->>New Supplier: registration
    Registration Service->>New Supplier: consent
    deactivate Registration Service
```

## Data Flows
