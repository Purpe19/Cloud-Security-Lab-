# Auditor IAM Read-Only Lab

## Objective
Test least-privilege IAM permissions for an Auditor user/group by allowing read-only access and preventing changes to AWS resources.

## Role Tested
Auditor

## AWS Services Tested
- IAM
- S3
- EC2
- CloudTrail
- CloudWatch

## Expected Permission
The Auditor should be able to view resources but should not be able to create, upload, delete, or modify resources.

## S3 Bucket
`dev-bucket-niranjan`

## Test Performed
1. Logged in as the Auditor IAM user.
2. Opened the AWS console.
3. Checked whether the Auditor could view IAM users/groups.
4. Checked whether the Auditor could view the S3 bucket.
5. Tried to upload a file to the S3 bucket.
6. Tried to delete or modify resources.

## Expected Result
- View IAM resources: Success
- View S3 bucket: Success
- Upload object to S3: Denied
- Delete object from S3: Denied
- Modify IAM permissions: Denied

## Security Explanation
The Auditor role should follow least privilege. Auditors need visibility into AWS resources for review and compliance, but they should not have permission to change production resources.

Read-only permissions usually use actions such as:

- `Get`
- `List`
- `Describe`
- `Lookup`

Write or dangerous permissions usually use actions such as:

- `Create`
- `Put`
- `Update`
- `Delete`
- `Attach`
- `Modify`

## Screenshot Evidence
Add screenshots here:

- Auditor IAM user or group
- Auditor policy attached
- Auditor successful read-only access
- Auditor upload denied
- Auditor delete denied

## What I Learned
I learned that an Auditor IAM role should be designed for visibility, not modification. This helps follow the least-privilege security model and reduces the risk of accidental or unauthorized changes.
