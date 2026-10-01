# AWS IAM Least-Privilege Security Project

## Project Overview

This project was able to demonstrate the implementation of AWS Identity and Access Management (IAM) using the principle of least privilege.

An IAM user was configured with restricted permissions to access a designated Amazon S3 project bucket while access to unauthorized AWS resources was denied. AWS CloudTrail was used to monitor and audit AWS activity.

---

## Project Screenshots

### 1. IAM Demo User

An IAM user was created to test least-privilege access to AWS resources.

![IAM Demo User](screenshots/Screenshot%202026-09-30-demo%20user.png)

---

### 2. IAM Permissions Defined

A custom IAM policy was configured to define the permissions available to the IAM user.

![IAM Permissions](screenshots/Screenshot%202026-09-30%20permissions%20defined.png)

---

### 3. Unauthorized AWS Services Denied

The IAM user was tested against AWS resources outside the permissions granted by the IAM policy. Access was denied as expected.

![Access Denied](screenshots/Screenshot%202026-09-30%20access-other-services%20denied.png)

---

### 4. Successful S3 File Upload

The IAM user successfully uploaded a file to the authorized project S3 bucket, demonstrating that the required S3 permissions were working.

![S3 File Upload](screenshots/Screenshot%202026-09-30%20file%20uploaded%20to%20project%20S3%20bucket.png)

---

### 5. PutObject Permission Test

The successful request demonstrates that the IAM user was authorized to perform the `s3:PutObject` operation against the designated project bucket.

![PutObject Request](screenshots/Screenshot%202026-09-30%20PutObject%20request%20accepted.png)

---

### 6. ListBucket Permission Test

The IAM user successfully listed objects within the authorized project S3 bucket while remaining restricted from unauthorized buckets.

![List Objects](screenshots/Screenshot%202026-09-30%20list%20object.png)

---

### 7. AWS CloudTrail Logs

AWS CloudTrail was used to monitor and audit AWS API activity associated with the project.

![CloudTrail Logs](screenshots/Screenshot%202026-09-30%20cloudtrail%20logs.png)

---

## Security Controls Demonstrated

- AWS IAM user management
- Least-privilege access control
- Customer-managed IAM policies
- Resource-level Amazon S3 permissions
- `s3:ListBucket`
- `s3:GetObject`
- `s3:PutObject`
- `s3:DeleteObject`
- Unauthorized-access testing
- Multi-Factor Authentication (MFA)
- AWS CloudTrail auditing and monitoring

---

## Key Takeaways

This project demonstrates how AWS IAM can be used to implement least-privilege access to cloud resources. The IAM user was granted only the permissions required to interact with the designated S3 project bucket while access to unauthorized resources remained restricted.

CloudTrail provided additional visibility into AWS activity, allowing API actions and security-related events to be reviewed for auditing and troubleshooting.

