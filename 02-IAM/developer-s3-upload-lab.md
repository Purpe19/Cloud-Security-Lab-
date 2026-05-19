# Developer IAM S3 Upload Lab

## Objective
Test least-privilege IAM permissions for a Developer user/group by allowing upload access to a specific S3 bucket.

## Role Tested
Developer

## Test File
`02-IAM/test-files/developer/developer-test-file.txt`

## S3 Bucket
`dev-bucket-niranjan`

## Expected Permission
The Developer should be able to upload a test file to the allowed S3 bucket.

## Test Performed
1. Created a test file named `developer-test-file.txt`.
2. Logged in as the Developer IAM user.
3. Opened the S3 bucket `dev-bucket-niranjan`.
4. Uploaded the test file.
5. Verified whether the upload succeeded.

## Result
The Developer user was able to upload the test file successfully.

## Security Explanation
This shows that the Developer role has permission to perform object upload actions such as `s3:PutObject` on the allowed bucket.

## Screenshot Evidence
Add screenshots here:

- Developer IAM user or group
- Developer policy attached
- S3 bucket upload page
- Successful upload confirmation

## What I Learned
I learned that IAM permissions can be tested by logging in as a specific IAM user and performing real actions in AWS. For S3 upload access, the user needs permission such as `s3:PutObject` on the object resource path.
