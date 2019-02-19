# AWS Well-Architected

https://aws.amazon.com/architecture/well-architected/

The Well-Architected Framework has been developed to help cloud architects build secure, high-performing, resilient, and efficient infrastructure for their applications. Based on five pillars — operational excellence, security, reliability, performance efficiency, and cost optimization — the Framework provides a consistent approach for customers and partners to evaluate architectures, and implement designs that will scale over time.

The framework is based on five pillars:
- Operational Excellence
- Security
- Reliability
- Performance Efficiency
- Cost Optimization

## Security

Security in the cloud is composed of five areas:

- Identity and access management
  - Protecting AWS credentials
    - IAM (groups, users), AWS STS (keys), MFA
  - Fine-grained authorizationcredentials
    - IAM (roles, policies)

- Detective controls
  - Capture and analyze logs
    - CloudTrail, CloudWatch Logs, GuardDuty, VPC Flow Logs, DNS logs, AWS Config, S3 & Glacier, Athena
  - Integrate auditing controls with notification and workflow
    - **CloudWatch Events**, AWS Config Rules, CloudWatch & CloudWatch Logs, CloudWatch API & AWS SDKs, Inspector
  
- Infrastructure protection
  - Protecting network and host-level boundaries
    - **VPC**, VPC Security Groups, Shield (DDoS protection), WAF (firewall), Firewall Manager, Direct Connect
  - System security configuration and maintenance
    - **Systems Manager**, Inspector (vulnerabilities), CloudFormation
  - Enforcing service-level protection
    - **IAM** (policies), AWS KMS, S3 (bucket policies), SNS 
  
- Data protection
  - Data classification
    - **resource tagging**, AWS KMS
  - Encryption/tokenization
    - AWS KMS, CloudHSM (hardware security module), DynamoDB (for storage)
  - Protecting data at rest
    - AWS KMS --> S3, EBS, Glacier
  - Protecting data in transit
    - ACM (AWS Certificate Manager), ELB, CloudFront
  - Data backup/replication/recovery
    - S3 (Cross-Region Replication, Lifecycle Policies and Versioning), EBS snapshot, RDS snapshots 

- Incident response
  - IAM -- grant appropriate authorization to incident response teams in advance
  - CloudFormation -- automate the creation of trusted environments for conducting deeper investigations
  - CloudTrail -- history of AWS API calls
  - CloudWatch Events -- trigger different automated actions
  - Step Functions -- coordinate a sequence if steps to automate an incident response
  
