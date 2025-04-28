# 🚀 Static Website Hosting on AWS S3

This project documents the process of hosting a static website (HTML, CSS, JS files) using an Amazon S3 bucket.  
S3 provides a low-cost and scalable solution for serving static websites directly to users over the internet.

---

## 📋 Steps Followed:

### 1. Create an S3 Bucket
- Go to **AWS Management Console → S3 → Create bucket**.
- Provide a globally unique bucket name (e.g., `your-website-bucket`).
- **Region**: Choose the region closest to your users.
- **Uncheck** the "Block all public access" option to allow public file access.
- Leave the rest of the settings default and create the bucket.

### 2. Upload Website Files
- Open the newly created bucket.
- Click **Upload** and add your static website files (`index.html`, `style.css`, `script.js`, images, etc.).
- After uploading, select the files → **Actions → Make public** (or modify permissions as needed).

### 3. Enable Static Website Hosting
- Go to the **Properties** tab of the bucket.
- Scroll to **Static website hosting** and **Enable** it.
- Set:
  - **Index document**: `index.html`
  - **Error document**: `error.html` (optional)
- Save changes.

### 4. Access Your Website
- After enabling static hosting, you will get a **Bucket website endpoint** like:
  ```
  http://your-website-bucket.s3-website-<region>.amazonaws.com
  ```
- Open this URL in your browser to view your live static website!

## 🛠️ Technologies Used
- AWS S3
- HTML, CSS, JavaScript (Static Files)
  AWS CloudFront (for future improvements)


# 📌 Note
Ensure that sensitive data is never uploaded to public S3 buckets.

