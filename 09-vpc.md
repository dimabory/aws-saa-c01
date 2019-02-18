# Amazon Virtual Private Cloud (Amazon VPC) 
https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html

Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure of AWS.

_Exam Tips_:
- Think of a VPC as a logical datacenter in AWS
- Consists of IGWs (or Virtual Private Gateways), Route Tables, Network Acces Control Lists, Subnets, and Security Groups
- 1 Subnet = 1 AZ
- Security groups are Stateful; Network Access Control List are Stateless;
- NO TRANSITIVE PEERING

---

- NAT instances
  - Disable Source/Destination Check on the instance
  - Must be in a public subnet
  - Must be a route out of the private subnet to the NAT instance, in order for this to work
  - The amount of traffic that NAT instance can support depends on the instance size
  - You can create high availability using Autoscaling Groups, multiple subnets in differenet AZs, and script to automate failover
  - Behind a Security Group
  
  
---

- NAT Gateways
  - Preffered by the enterprise
  - Scale automatically up to 10Gb/s
  - No need to pathc
  - Not associated with security groups
  - Automatically assigned a public IP
  - Remeber to update your route tables
  - No need to disable Source/Destination Checks
  - More secure than a NAT instance
  
---

- Network ACLs
  - Your VPC automatically comes a default network ACL, and by default it allows all outbount and inbound traffic
  - You can create custom network ACLs. By default, each custom network ACL denies all inbound and outbound traffic until you add rules
  - Each subnet in your VPC must be associated with a network ACL. If you don't explicitly associate a subnet with a network ACL, the subnet is automatically associated with the default network ACL
  - You can associate a network ACL with multiple subnets; however, a subnet can be associated with only one network ACL at a time. When you associate a network ACL with a subnet, the previous association is removed
  - Network ACLs contain a numbered list of rules that is evaluated in order, starting with the lowest numbered tule
  - Network ACLs have separate in/out -bound rules, each rule can either allow or deny  
  - Network ACLs are stateless; responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa)
  - Block IP Addresses using network ACLs not Security Groups

---

- ALB's
  - You'll need at least 2 public subnets in order to deploy an application load balancer
  
---

- VPC Flow Logs 
  - You can't enable flow logs for VPCs that are peered with your VPC unless the peer VPC is in your account
  - You can't tag a flow log
  - After you've created a flow log, you can't change its config; for example, you can't associate a different IAM role with the flow log
  - Not all IP traffic is monitored
    - genereted by the Amazon DNS server (your own DNS server is OK)
    - by a Windows instances for Amazon Windows license activation
    - to/from 169.254.169.254
    - DHCP
    - reserved IP address for the default VPC router

---

- VPC Endpoints
