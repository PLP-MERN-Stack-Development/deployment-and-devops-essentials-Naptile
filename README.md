🚀 Deployment and DevOps Essentials MERN App

A full MERN stack application deployed using modern DevOps practices.
This project demonstrates:

Deployment of the backend (Express API) on Render

Deployment of the frontend (React) on Render Static Hosting

Implementation of CI/CD pipelines using GitHub Actions

Use of environment variables for secure configuration

Basic monitoring practices

Production-ready folder structure and deployment scripts

This README explains every step taken in the process and meets all assignment requirements.

📁 Project Repository

🔗 GitHub Repo:
https://github.com/PLP-MERN-Stack-Development/deployment-and-devops-essentials-Naptile.git

📦 Project Structure
deployment-and-devops-essentials-Naptile/
│
├── client/                 # React frontend
├── server/                 # Express backend
│
├── deployment/             # Deployment configs
├── monitoring/             # Monitoring scripts & examples
│
├── .github/workflows/      # CI/CD pipelines
├── .env.example            # Sample environment variables
│
├── Week7-Assignment.md     # Instructions provided by course
└── README.md               # (This file)

🌐 Live Application URLs
Frontend (React)

🔗 https://deployment-and-devops-essentials-naptile-eo2v.onrender.com/

Backend (Express API)

🔗 https://deployment-and-devops-essentials-naptile.onrender.com/

Test endpoint:

https://deployment-and-devops-essentials-naptile.onrender.com/api

⚙️ Backend Deployment (Render)

The backend was deployed as a Web Service on Render.

✔ Steps taken:

Created a new Web Service on Render

Connected GitHub repository

Configured environment variables:

PORT=5000
MONGO_URI=<MongoDB Atlas connection string>


Set build and start commands:

Build Command: npm install

Start Command: node server.js

✔ Backend CI/CD

Render automatically redeploys when:

GitHub Actions triggers a deployment, or

You push to main

Your backend GitHub Actions workflow uses:

service-id: srv-d4c4pgv5r7bs73a69hug

🎨 Frontend Deployment (Render Static Hosting)

The frontend was deployed using Render Static Hosting.

✔ Build settings:

Build Command:

npm install && npm run build


Publish Directory:

build


Render automatically rebuilds and redeploys when GitHub Actions pushes a new build.

🔄 CI/CD Pipeline (GitHub Actions)

The project includes 4 pipelines:

Workflow	Purpose
frontend-ci.yml	Build & test React app
backend-ci.yml	Test Express server and linting
frontend-cd.yml	Deploy frontend to Render
backend-cd.yml	Deploy backend to Render
✔ Secrets used:

Go to GitHub → Settings → Secrets → Actions and add:

Name	Purpose
RENDER_API_KEY	Deploys services on Render
🧪 How to Run Locally
1. Clone the project
git clone https://github.com/PLP-MERN-Stack-Development/deployment-and-devops-essentials-Naptile.git
cd deployment-and-devops-essentials-Naptile

2. Install dependencies
Backend:
cd server
npm install

Frontend:
cd ../client
npm install

3. Create environment files

Create server/.env:

PORT=5000
MONGO_URI=< MongoDB connection string>

4. Start the backend
cd server
node server.js

5. Start the frontend
cd client
npm start

📊 Monitoring

The /monitoring folder includes:

Example logs setup

Healthcheck scripts

Commands for tracking uptime

Example pm2 config (if needed in future)

Basic monitoring used for this assignment:

Manual uptime checks

Render dashboard monitoring

API responsiveness testing

