Long Term Key

```shell
aws configure --profile [profile-name] # To configure programmatic access
```

short Term key

```
aws configure set aws_assess_key_id [key-id] --profile [profile-name]
aws configure set aws_secret_access_key [key-id] --profile [profile-name]
aws configure set aws_session_token [token] --profile [profile-name]
```

Get Details of Security Token Service (STS)

```shell
aws sts get-caller-identify --profile [profile-name] # Get details belongs to profile
```

# Enum

USERS

```shell

aws iam list-users --profile [profile-name] # List all IAM users in the specified AWS account._
    
aws iam list-groups-for-user --user-name [user-name] --profile [profile-name] # List all groups to which the specified IAM user belongs.
    
aws iam list-user-policies --user-name [username] --profile [profile-name] # List all inline policies directly attached to the specified IAM user.
    
aws iam get-user-policy --user-name user-name --policy-name [policy-name] # Retrieve the details of a specific inline policy attached to the specified IAM user.

aws iam list-attached-user-policies --user-name [username] --profile [profile-name] # List all managed policies attached to the specified IAM user.

aws iam get-policy --policy-arn [policy-arn] # Retrieve metadata about a specific managed policy using its ARN.
```

GROUPS

```shell

aws iam list-groups --profile [profile-name] # List all IAM groups in the specified AWS account.
    
aws iam get-group --group-name [grp-name] --profile [profile-name] # List all IAM users in the specified IAM group.
    
aws iam list-group-policies --group-name [group-name] --porfile-name [profile-name] # List all inline policies directly attached to the specified IAM group.
    
aws iam get-group-policy --group-name group-name --policy-name [policy-name] # Retrieve the details of a specific inline policy attached to the specified IAM group.

aws iam list-attached-groups-policies --group-name [grp-name] --profile-name [profile-name] # List all managed policies attached to the specified IAM group.

aws iam get-policy --policy-arn [policy-arn] # Retrieve metadata about a specific managed policy using its ARN.

```

ROLES

```shell
aws iam list-roles # List all IAM roles in the specified AWS account.
    
aws iam list-role-policies --role-name [role-name] # List all inline policies directly attached to the specified IAM role.
    
aws iam get-role-policy --role-name role-name --policy-name [policy-name] # Retrieve the details of a specific inline policy attached to the specified IAM role.

aws iam list-attached-role-policies --role-name [role-name] # List all managed policies attached to the specified IAM role.

aws iam get-policy --policy-arn [policy-arn] # Retrieve metadata about a specific managed policy using its ARN.
```

POLICIES

```shell
aws iam list-policies # List all managed policies in the specified AWS account._
    
aws iam get-policy --policy-arn [policy-arn] # Retrieve metadata about a specific managed policy using its ARN.
    
aws iam list-policy-versions --policy-arn [policy-arn] # List all versions of a specified managed policy.
    
aws iam get-policy-version --policy-arn policy-arn --version-id [version-id] # Retrieve the details of a specific version of a managed policy.
```

S3 Bucket

```bash
aws s3 ls s3://bucket-name/F1 --no-sign-request # Without credentials
aws s3 ls s3://bucket-name/F1 --profile [profile-name] # With credentials
aws s3 cp s3://bucket-name/source  [distination] # Copy files
```