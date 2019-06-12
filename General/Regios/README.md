# Regions, AZs, Edge locations

## Regions

- One country can have multiple regions
  - us-west-1
  - us-east-1
- Provides an availability to isolate data and systems in certain area of the world
  - Prevents global failures (political decisions, war)
- Contains availability zones

## Availability zones

- Fault isolation domain
  - Prevents local failures (fire, flood)
  - Infrastructure should be spread out across availability zones
- Represent physical data center
  - us-east-1a
  - us-east-1b
- High performance networking between each other

## Edge locations

- Distributed globally in major cities
- Used by CloudFront (CDN) to distribute content to end user
