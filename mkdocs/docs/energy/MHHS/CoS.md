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

### Data Flows
The Central Switching Service design documentation is [listed at Ofgem](https://www.ofgem.gov.uk/publications/css-design-and-delivery-products) along with the [end-to-end design products](https://www.ofgem.gov.uk/publications/e2e-design-products).    

|Sequence |Flow |Definition |
|:-|:-|:-|
|1 |CSS1800 ||
