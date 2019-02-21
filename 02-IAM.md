# Identity Access Management (IAM)

https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html \
https://github.com/awsdocs/iam-user-guide/blob/master/doc_source/introduction.md

**AWS Identity and Access Management (IAM)** is a web service that helps you securely control access to AWS resources. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.

When you first create an AWS account, you begin with a single sign-in identity that has complete access to all AWS services and resources in the account. This identity is called the AWS account root user and is accessed by signing in with the email address and password that you used to create the account. We strongly recommend that you do not use the root user for your everyday tasks, even the administrative ones. Instead, adhere to the best practice of using the root user only to create your first IAM user. Then securely lock away the root user credentials and use them to perform only a few account and service management tasks.

---
_Allows to manage_:

- Users;
- Groups;
- Roles;
- Policies.

Example of policy:
```
{
  "Version": "2012-10-17",
  "Statement": {
    "Effect": "Allow",
    "Action": "dynamodb:*",
    "Resource": "arn:aws:dynamodb:us-east-2:123456789012:table/Books"
  }
}
```

---
_Exam Tips_:

- IAM is universal (global).
- "root account" - full admin access.
- New users have NO permissions at all when first created.
- Access Key Id & Secret Access Keys are used to access AWS via APIs and CLI.
- ALWAYS setup MFA on the root account.
- Root can create & customise password rotation policies.

