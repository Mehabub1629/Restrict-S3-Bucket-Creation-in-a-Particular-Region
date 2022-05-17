# Restrict-S3-Bucket-Creation-in-a-Particular-Region
Restricting a user from creating an amazon S3 bucket in a particular region by creating a policy.
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Deny",
            "Action": "s3:*",
            "Resource": "*",
            "Condition": {
                "StringNotEquals": {
                    "aws:RequestedRegion": [
                        "us-east-1",
                        "ap-south-1"
                    ]
                }
            }
        }
    ]
}
