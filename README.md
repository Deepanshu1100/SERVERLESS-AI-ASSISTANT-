# 🤖 AI Personal Assistant — AWS Workshop

> Build a fully functional AI Personal Assistant using **Amazon Bedrock**, **AWS Lambda**, **DynamoDB**, and **API Gateway** — in just 3 days!

![Architecture](assets/architecture.png)

---

## 🚀 Live Demo

**Frontend:** [http://ai-assistant-frontend8909.s3-website.eu-north-1.amazonaws.com](http://ai-assistant-frontend8909.s3-website.eu-north-1.amazonaws.com)

---

## 🏗️ Architecture

```
User
  ↓
Frontend (HTML/JS) — hosted on S3
  ↓
API Gateway (REST API — POST /chat)
  ↓
AWS Lambda (Python — business logic)
  ↓              ↓
Amazon Bedrock   DynamoDB
(Claude AI)    (Chat History)
  ↓
Response returned to User
```

---

## 📅 Workshop Structure

| Day | Theme | What You Build |
|-----|-------|----------------|
| **Day 1** | Foundation | Lambda function that calls Amazon Bedrock (Claude AI) |
| **Day 2** | Backend | DynamoDB chat history + REST API via API Gateway |
| **Day 3** | Frontend & Deploy | Chat UI deployed live on AWS S3 |

---

## 🛠️ Tech Stack

| Service | Purpose |
|---------|---------|
| Amazon Bedrock | Claude AI model — generates responses |
| AWS Lambda | Python backend — business logic |
| DynamoDB | Stores full conversation history |
| API Gateway | Exposes REST API to the world |
| AWS S3 | Hosts the frontend (HTML/CSS/JS) |
| IAM | Roles and permissions |

---

## 📁 Folder Structure

```
ai-personal-assistant/
├── day-1/
│   ├── lambda_function.py      # Lambda + Bedrock basic call
│   └── README.md               # Day 1 step-by-step guide
├── day-2/
│   ├── lambda_function.py      # Lambda + DynamoDB + API Gateway
│   └── README.md               # Day 2 step-by-step guide
├── day-3/
│   ├── index.html              # Complete chat frontend
│   └── README.md               # Day 3 step-by-step guide
├── assets/
│   └── architecture.png        # Architecture diagram
├── .gitignore
└── README.md                   # This file
```

---

## ⚙️ Prerequisites

- AWS Account (Free Tier is enough)
- Basic Python or JavaScript knowledge
- Laptop with internet connection
- VS Code or any code editor

---

## 🔑 AWS Services Setup Checklist

- [ ] AWS Account created
- [ ] Region set to `us-east-1` (for Bedrock) 
- [ ] Bedrock Model Access enabled (Claude 3 Haiku / Sonnet)
- [ ] IAM Role created with `AmazonBedrockFullAccess` + `AWSLambdaFullAccess` + `AmazonDynamoDBFullAccess`
- [ ] Lambda function created (`ai-assistant`)
- [ ] DynamoDB table created (`chat-history`)
- [ ] API Gateway created (`ai-assistant-api`)
- [ ] S3 bucket created with static website hosting enabled

---

## 🚦 Quick Start

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/ai-personal-assistant.git
cd ai-personal-assistant
```

### 2. Day 1 — Deploy Lambda + Bedrock
- Go to `day-1/` folder
- Follow `day-1/README.md`

### 3. Day 2 — Add DynamoDB + API Gateway
- Go to `day-2/` folder
- Follow `day-2/README.md`

### 4. Day 3 — Deploy Frontend
- Go to `day-3/` folder
- Follow `day-3/README.md`

---

## 💡 Key Features

- 🧠 **AI-powered responses** via Claude on Amazon Bedrock
- 💾 **Persistent memory** — conversation history stored in DynamoDB
- 🌐 **REST API** — accessible from any device via API Gateway
- 🎨 **Beautiful chat UI** — deployed live on AWS S3
- 🔒 **Secure** — IAM roles and permissions properly configured

---

## 📸 Screenshots

### Chat Interface
> Live chat UI with AI responses and conversation memory

---

## 🙌 Workshop Credits

Built with ❤️ during the **AWS AI Developer Workshop**

**Technologies:** Amazon Bedrock · AWS Lambda · DynamoDB · API Gateway · S3

---

## 📄 License

MIT License — free to use and modify!
