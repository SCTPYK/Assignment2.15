# Assignment2.15
What is needed to authorize your EC2 to retrieve secrets from the AWS Secret Manager?
1. Ec2 might require IAM role that has "secretsmanager:GetSecretValue"

Derive the IAM policy (i.e. JSON)?
```
{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "VisualEditor0",
			"Effect": "Allow",
			"Action": "secretsmanager:GetSecretValue",
			"Resource": "arn:aws:secretsmanager:us-east-1:255945442255:secret:prod/cart-service/credentials-exampleidfromconsole"
		}
	]
}
```
Using the secret name prod/cart-service/credentials, derive a sensible ARN as the specific resource for access
arn:aws:secretsmanager:us-east-1:255945442255:secret:prod/cart-service/credentials-exampleidfromconsole
