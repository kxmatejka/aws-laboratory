# IAM

Identity & Access Management

- Allows control and access to AWS services and resources
- It is a global service. Pool of identities is shared across all regions
- IAM manages:
  - Users
  - Groups
  - IAM Policies
  - Authentication attributes (usernames, passwords, access keys, MFA, password policies)

## IAM JSON Policy Elements

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:*",
      "Resource": "*"
    }
  ]
}
```

- Effect
  - Determines what the statement does
  - Allow | Denied
- Action
  - Specifies one or more api to which statement will affect
  - \* | s3:\* | s3:GetObject | [ s3:\*, sqs:\* ]
- Resource
  - Specifies resource in arn format to which statement will affect
  - arn:aws:s3:::my_corporate_bucket/\*
- see also: NotAction, NotResource, Condition
