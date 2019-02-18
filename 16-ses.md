# Amazon Simple Email Service (Amazon SES)
https://docs.aws.amazon.com/ses/latest/DeveloperGuide/Welcome.html

Amazon SES is an email platform that provides an easy, cost-effective way for you to send and receive email using your own email addresses and domains.

For example, you can send marketing emails such as special offers, transactional emails such as order confirmations, and other types of correspondence such as newsletters. When you use Amazon SES to receive mail, you can develop software solutions such as email autoresponders, email unsubscribe systems, and applications that generate customer support tickets from incoming emails.

Building a large-scale email solution is often a complex and costly challenge for a business. You must deal with infrastructure challenges such as email server management, network configuration, and IP address reputation. Additionally, many third-party email solutions require contract and price negotiations, as well as significant up-front costs. Amazon SES eliminates these challenges and enables you to benefit from the years of experience and sophisticated email infrastructure Amazon.com has built to serve its own large-scale customer base.

Amazon SES integrates seamlessly with other AWS products. For example, you can:

- Add email-sending capabilities to any application. If your application runs in Amazon Elastic Compute Cloud (Amazon EC2), you can use Amazon SES to send 62,000 emails every month at no additional charge. You can send email from Amazon EC2 by using an AWS SDK, by using the Amazon SES SMTP interface, or by making calls directly to the Amazon SES API.

- Use AWS Elastic Beanstalk to create an email-enabled application such as a program that uses Amazon SES to send a newsletter to customers.

- Set up Amazon Simple Notification Service (Amazon SNS) to notify you of your emails that bounced, produced a complaint, or were successfully delivered to the recipient's mail server. When you use Amazon SES to receive emails, your email content can be published to Amazon SNS topics.

- Use the AWS Management Console to set up Easy DKIM, which is a way to authenticate your emails. Although you can use Easy DKIM with any DNS provider, it is especially easy to set up when you manage your domain with Route 53.

- Control user access to your email sending by using AWS Identity and Access Management (IAM).

- Store emails you receive in Amazon Simple Storage Service (Amazon S3).

- Take action on your received emails by triggering AWS Lambda functions.

- Use AWS Key Management Service (AWS KMS) to optionally encrypt the mail you receive in your Amazon S3 bucket.

- Use AWS CloudTrail to log Amazon SES API calls that you make using the console or the Amazon SES API.

- Publish your email sending events to Amazon CloudWatch or Amazon Kinesis Data Firehose. If you publish your email sending events to Kinesis Data Firehose, you can access them in Amazon Redshift, Amazon Elasticsearch Service, or Amazon S3.
