# tachecks

It is AWS TrustedAdvisor multi-account crawler. Run this CloudFormation template in your master account and it will create a micro instance which will check your TrustedAdvisor across all linked accounts that you specify in the template. Then it will create one CSV file with all checks in the S3 bucket you specify. It also creates a role that can perform those checks along with the instance profile. It is needed to access your TA checks in other accounts from your new instance. You can use your default VPC.

Pre-requisites:
- Administrative IAM user that can run the CloudFormation template in master account
- S3 bucket which will be used to store your TA checks
- Default role created by AWS Organizations during account creation. Role name: "OrganizationAccountAccessRole"
