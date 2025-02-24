## AWS IAM

- List AWS Roles:
```bash
 aws iam list-roles
{
    "Roles": [
        {
            "Path": "/",
            "RoleName": "awss3",
            "RoleId": "AROA2ISJARIZ5TRDRSAHSHASHAS",
            "Arn": "arn:aws:iam::705663420027:role/awss3",
            "CreateDate": "2024-06-24T19:09:53+00:00",
            "AssumeRolePolicyDocument": {
                "Version": "2012-10-17",
                "Statement": [
                    {
                        "Effect": "Allow",
                        "Principal": {
                            "Service": "s3.amazonaws.com"
                        },
                        "Action": "sts:AssumeRole"
                    }
                ]
            },
            "Description": "Allows S3 to call AWS services on your behalf.",
            "MaxSessionDuration": 3600
        }
```

- List AWS Roles using `grep` command to filter "RoleName":
```bash
$ aws iam list-roles | grep RoleName
            "RoleName": "awss3",
            "RoleName": "AWSServiceRoleForOrganizations",
            "RoleName": "AWSServiceRoleForSSO",
            "RoleName": "AWSServiceRoleForSupport",
            "RoleName": "AWSServiceRoleForTrustedAdvisor",
            "RoleName": "cloud-formation-service-role",
            "RoleName": "homelab-lambda-function-allows-ec2",
            "RoleName": "lambda-full-access-service-role",
            "RoleName": "lambdatest2",
            "RoleName": "role-teste-2",
            "RoleName": "role-teste-aws-rds",
            "RoleName": "teste-lambda-role-q4mkc3ln",
            "RoleName": "teste1",
            "RoleName": "testecloud-formtion",
```

- List AWS Roles using the `wc -l` command to count:
```bash
$ aws iam list-roles | grep RoleName | wc -l
14
```
## AWS EC2
- Run the command to list the security groups:
```bash
$ aws ec2 describe-security-groups | grep GroupName
            "GroupName": "launch-wizard-6",
            "GroupName": "launch-wizard-12",
            "GroupName": "default",
            "GroupName": "launch-wizard-15",
            "GroupName": "launch-wizard-5",
            "GroupName": "launch-wizard-9",
            "GroupName": "launch-wizard-8",
            "GroupName": "ec2group1234",
            "GroupName": "launch-wizard-17",
            "GroupName": "launch-wizard-19",
            "GroupName": "default",
            "GroupName": "launch-wizard-18",
```