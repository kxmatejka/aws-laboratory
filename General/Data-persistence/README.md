# Data Persistence

## Ephemeral

- Data that is generally local to a resource and is lost when that resource is powered down
- Fastest storage
- Useful for temporary storage, cache, local database
- Amazon ElasticCache, Amazon EC2 storage

## Transient

- Data that exists in a form while it's passed between sources
- Amazon SQS

## Persistent

- Data that is durable and survives power events
- Accessible through network with worse performance than ephemeral storage
- Amazon EBS, Amazon EFS
