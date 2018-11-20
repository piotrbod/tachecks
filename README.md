# tachecks

It is AWS TrustedAdvisor multi-account crawler. Run this CloudFormation template in your master accout and it will create a micro instance which will check your TrustedAdvisor across all linked accounts that you specify in the template. Then it will create one CSV file with all checks in the S3 bucket you specify. It also creates a role that can do it along with the instance profile which is needed to access your TA checks in other accounts.
