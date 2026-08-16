Deployment-Steps# AWS S3 Static Website Deployment

## Deployment Steps

### Step 1: Create an S3 Bucket

1. Open the **AWS Management Console**.
2. Navigate to **Amazon S3**.
3. Click **Create bucket**.
4. Enter the bucket name:
   `personal-portfolio-intership-1st-project`
5. Select the AWS Region:
   `Asia Pacific (Mumbai) - ap-south-1`
6. Click **Create bucket**.

### Step 2: Disable Block Public Access

1. Open the `personal-portfolio-intership-1st-project` bucket.
2. Go to the **Permissions** tab.
3. Under **Block public access**, click **Edit**.
4. Disable **Block all public access**.
5. Confirm the warning.
6. Click **Save changes**.

### Step 3: Upload Website Files

1. Open the **Objects** tab.
2. Click **Upload**.
3. Upload:
   - `index.html`
   - `profile.jpg`
4. Click **Upload**.

The bucket should contain:

    personal-portfolio-intership-1st-project/
    ├── index.html
    └── profile.jpg

### Step 4: Configure Bucket Policy

1. Go to **Permissions → Bucket policy**.
2. Add the following policy:

    {
      "Version": "2012-10-17",
      "Statement": [
        {
          "Sid": "PublicReadGetObject",
          "Effect": "Allow",
          "Principal": "*",
          "Action": "s3:GetObject",
          "Resource": "arn:aws:s3:::personal-portfolio-intership-1st-project/*"
        }
      ]
    }

3. Click **Save changes**.

### Step 5: Enable Static Website Hosting

1. Go to the **Properties** tab.
2. Scroll to **Static website hosting**.
3. Click **Edit**.
4. Select **Enable**.
5. Select **Host a static website**.
6. Set the **Index document** to:
   `index.html`
7. Click **Save changes**.

### Step 6: Get the Website Endpoint

1. Stay in the **Properties** tab.
2. Scroll to **Static website hosting**.
3. Copy the **Bucket website endpoint**.
4. Open the endpoint in a web browser.

### Step 7: Verify the Website

Verify that the deployed portfolio displays:

- AWS Cloud Engineer introduction
- Profile photo
- About section
- Technical skills
- AWS projects
- Learning credentials
- Cloud journey
- Contact section

### Deployment Architecture

    Internet
        │
        ▼
    Amazon S3
        │
        ▼
    Static Website Hosting
        │
        ├── index.html
        │
        └── profile.jpg
        │
        ▼
    AWS Cloud Engineer Portfolio

### Deployment Flow

    Create S3 Bucket
          ↓
    Disable Block Public Access
          ↓
    Upload index.html + profile.jpg
          ↓
    Configure Bucket Policy
          ↓
    Enable Static Website Hosting
          ↓
    Set index.html as Index Document
          ↓
    Get Website Endpoint
          ↓
    Open Live Portfolio
