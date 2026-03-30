# Day 3 — Frontend + Deploy on AWS S3

## 🎯 Goal
Build a beautiful chat interface and deploy it live on AWS S3.

## ✅ What You Will Build
A fully working AI Personal Assistant accessible from any browser — deployed on AWS!

---

## 🛠️ Step-by-Step Setup

### Step 1 — Update API URL in index.html
Open `index.html` and find this line:
```javascript
const API_URL = 'YOUR_API_GATEWAY_URL/chat';
```
Replace with your actual API Gateway Invoke URL from Day 2.

---

### Step 2 — Create S3 Bucket
1. AWS Console → **S3** → **"Create bucket"**
2. Settings:
   - Bucket name: `ai-assistant-frontend-[any number]`
   - Region: same as your setup
   - Block all public access: ❌ **Turn OFF**
3. Click **"Create bucket"**

---

### Step 3 — Enable Static Website Hosting
1. S3 bucket → **"Properties"** tab
2. Scroll down → **"Static website hosting"** → **"Edit"**
3. Enable it
4. Index document: `index.html`
5. Click **"Save changes"**

---

### Step 4 — Add Bucket Policy (Public Read)
1. S3 bucket → **"Permissions"** tab
2. **"Bucket policy"** → **"Edit"**
3. Paste this (replace `YOUR-BUCKET-NAME`):
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}
```
4. Click **"Save changes"**

---

### Step 5 — Upload index.html
1. S3 bucket → **"Objects"** tab
2. Click **"Upload"** → **"Add files"**
3. Select `index.html`
4. Click **"Upload"**

---

### Step 6 — Get Your Live URL
1. S3 bucket → **"Properties"** tab
2. Scroll to **"Static website hosting"**
3. Copy the **"Bucket website endpoint"**
4. Open in browser — your AI Assistant is live! 🎉

---

## 📦 Files
- `index.html` — Complete chat interface (HTML + CSS + JS)

---

## 🔑 Key Concepts Learned
- Building a frontend with HTML/CSS/JS
- Connecting frontend to a REST API
- Hosting a static website on AWS S3
- Full-stack deployment on AWS
