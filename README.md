# Static Website Hosting on AWS S3

## Project Overview
This project demonstrates how to host a static website using Amazon S3. It includes creating an S3 bucket, enabling static website hosting, configuring public access, and uploading website files.

## Features
- Static website hosting using Amazon S3
- Public access enabled using bucket policy
- Website accessible through S3 website endpoint
- Simple HTML, CSS, JS website deployment

## AWS Services Used
- Amazon S3
- IAM (for permissions)

## Project Structure
.
├── index.html
└── screenshots/
    ├── 01-bucket-overview.png
    ├── 02-static-website-hosting.png
    ├── 03-bucket-policy.png
    ├── 04-files-uploaded.png
    └── 05-website-output.png

## Steps to Deploy Website on S3

### 1. Create an S3 Bucket
- Choose a unique bucket name.
- Select a region.
- Keep the bucket public (required for static website hosting).

### 2. Upload Website Files
Upload files such as:
- index.html
- error.html (optional)

### 3. Enable Static Website Hosting
Go to Properties -> Static website hosting.
- Enable hosting
- Index document: index.html
- Error document: error.html

### 4. Set Bucket Policy (Public Read Access)
Use the following policy and replace your-bucket-name with your actual bucket name:
{
"Version": "2012-10-17",
"Statement": [
{
"Effect": "Allow",
"Principal": "",
"Action": "s3:GetObject",
"Resource": "arn:aws:s3:::your-bucket-name/"
}
]
}

### 5. Disable Block Public Access
Go to Permissions -> Block Public Access.
Turn off the settings and confirm by typing "confirm".

### 6. Access Your Website
Use the S3 website endpoint URL:
http://your-bucket-name.s3-website-region.amazonaws.com

### Screenshots
Screenshots included:
1.Bucket overview
2.Static hosting page
3.Bucket policy
4.Uploaded files
5.Final website output

### Learning Outcome
Through this project, I learned:
* How to host a static website using Amazon S3
* How to configure bucket permissions
* How to make a bucket public
* How to use the AWS console effectively

