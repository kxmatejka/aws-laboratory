# VPC

## Virtual Private Cloud Essentials

VPC enables you to launch AWS resources into a virtual network.

![vpc overview](aws-vpc-overview.png)

### Features

- private/public subnets
- ability to extend network to the cloud as if it was part of your network

### Properties

- VPC is housed within a chosen AWS region
- VPC spans multiple availability zones within a region
- AWS provides a DNS server for you VPC. You can run your own DNS server by changing DHCP

### Default VPC

- created with account
  - can be deleted and recreated
  - allowed only one default vpc per account
- all subnets have a route to the internet
- each instance in default VPC (by default) has a private and public IP

### Limits

- 5 VPCs per region
- 5 internet GW per region
- 5 elastic IP
- 50 VPN connections per region

### Routing

- VPC Router is highly available service
- VPC Router using first address of ip range
- VPC have main route table which is implicit to each subnet
- Each subnet have just one route table

### Network ACL

- Subnet can have only one associated NACL (but one NACL can be associated to many subnets)
- NACL can control inbound and outbound traffic
- By default the're allowing all inbound and outbound traffic
- NACL is stateless. NACL don't know if traffic is initialized or a response to.
- Rules are processed in ascending rule number.
- It can be used as a quick anti-ddos tool.
- NACL can't affect traffic between instances within same subnet
- NACL can be configured only by a range of IP addresses.

### Security groups

- SG are applied to network interfaces
- SG are statefull (inbound rule covers outbound traffic and conversely)
- SG don't have order of evaluation
- Any traffic which is not covered by any rule is implicitly denied
- SG can reference to any other aws resource
