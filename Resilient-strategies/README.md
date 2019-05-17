# Resilient strategies

## High availability

- System can recovery from failure
  - if it fails, it can take time to recover
- Minimizes availability issues

## Fault tolerant

- System can operate through failure
  - if anything fails, it has a replacement
  - system don't have an outage
- System is also high available
- That is achieved by redundancy
  - services placed across multiple availability zones

## Disaster recovery

- System protecting critical data from which is able to re-create a new working system
- Any system should have an disaster recovery plan

### Recovery point objective (RPO)

- The time between when a disaster occurs and the last recoverable copy of key business data was created
- If backup is created once per a day then RPO can be 24 hours
- Define amount of data that you will lose

### Recovery time objective (RTO)

- The time between when a disaster occurs and when the system can be restored to an operational state and handed over to the business for testing
