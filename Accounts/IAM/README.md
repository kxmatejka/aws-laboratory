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

### Basic usage

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
- see also: NotAction, NotResource, [Condition](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements_condition.html)

### Condition

This condition allows to list files in `test-bucket/some-user`

```json
{
  "Statement": [
    {
       "Action": ["s3:ListBucket"],
       "Effect": "Allow",
       "Resource": ["arn:aws:s3::test-bucket"],
       "Condition": {
         "StringLike": {
           "s3:prefix": ["some-user/*"]
         }
       }
    }
  ]
}
```

- IAM supports [several variables](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_variables.html) 
- For example a user name
```
"Condition": {"StringLike": {"s3:prefix": ["${aws:username}/*"]}}
```
