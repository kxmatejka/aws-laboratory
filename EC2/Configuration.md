# Configuration

## Metadata & user data

Data is not protected by any cryptographic method. Anyone who can access the instance can view its metadata.

[docs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html)

### Retrieving Instance Metadata

```bash
curl http://169.254.169.254/latest/meta-data/
```
