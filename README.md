# 🌸 AI-Based Employee Wellness Management

## 📌 Project Overview

**AI-Based Employee Wellness Management** is a web-based application designed to help employees monitor and understand their emotional and overall wellness.

The system combines **mood tracking, journal-based NLP analysis, face-based emotion analysis, AI wellness chat, weekly wellness reports, and dashboards** to provide meaningful insights into employee well-being.

The application also provides role-based access for **Employees and Managers**, along with secure authentication and database storage.

---

## 🎯 Objectives

* Track employees' daily moods and wellness information.
* Analyze journal text using NLP techniques.
* Detect emotions from facial expressions using AI-based face analysis.
* Provide a supportive AI-powered Wellness Chat.
* Generate weekly wellness scores and reports.
* Visualize mood, stress, sleep, emotions, and wellness trends.
* Provide personalized recommendations and achievements.
* Allow users to download weekly wellness reports as PDF.
* Provide managers with team-level wellness analytics.

---

## ✨ Key Features

### 🔐 1. Secure User Authentication

* Employee and Manager registration.
* Login using email and password.
* Password hashing for secure storage.
* Email OTP verification.
* Forgot-password and password-reset functionality.
* JWT-based authentication and session management.

### 😊 2. Mood Tracking

Employees can record their daily mood, such as:

* Amazing
* Happy
* Normal
* Sad
* Angry

The recorded mood information is stored and used for wellness analytics.

### 📝 3. Journal & NLP Analysis

Employees can write about their daily experiences and feelings.

The NLP module analyzes the journal text to identify:

* Sentiment
* Emotion
* Confidence
* Positive, negative and neutral sentiment scores

The analyzed information is used in dashboards and weekly reports.

### 📷 4. Face-Based Emotion Analysis

The application allows users to capture a face image using the camera.

The system analyzes the facial expression and provides:

* Detected emotion
* Confidence percentage

> **Note:** This feature is used for emotion analysis and is not used for identifying the person's identity.

### 💬 5. AI Wellness Chat

The Wellness Chat provides a supportive conversational space where employees can share how they are feeling.

The AI assistant processes the user's message and provides a supportive response.

> The Wellness Chat is intended as a wellness-support feature and is not a substitute for professional care.

### 📊 6. Weekly Wellness Report

The system generates a 7-day wellness report using available stored data.

The report includes:

* Overall Wellness Score
* Data Coverage
* Average Stress
* Average Sleep
* Most Common Mood
* Most Common Emotion
* Journal Activity
* Emotion Confidence
* Daily Wellness Scores
* Mood trends
* Stress trends
* Sleep trends
* Emotion distribution
* Emotion frequency
* Sentiment analysis
* AI-generated weekly summary
* Personalized recommendations
* Achievements

### 📄 7. PDF Report

Users can download the generated weekly wellness report as a **PDF file** for future reference.

### 📈 8. Wellness Dashboard

The dashboard provides visual analytics such as:

* Mood distribution
* Mood trends
* Detected emotions
* Recent wellness activity

Managers can also view team-level wellness information.

---

## 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │       User           │
                    │ Employee / Manager   │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   Streamlit UI       │
                    │     Frontend         │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    FastAPI Backend   │
                    │   Python / Uvicorn   │
                    └──────┬───────┬───────┘
                           │       │
             ┌─────────────┘       └─────────────┐
             ▼                                   ▼
   ┌──────────────────┐                ┌──────────────────┐
   │ PostgreSQL / Neon│                │ AI / NLP Modules │
   │     Database     │                │                  │
   └──────────────────┘                └────────┬─────────┘
                                                │
                                  ┌─────────────┼─────────────┐
                                  ▼             ▼             ▼
                               NLP        Face Emotion    Wellness
                              Analysis      Analysis        Chat
```

---

## 🛠️ Technology Stack

### Frontend

* Python
* Streamlit
* HTML/CSS

### Backend

* Python
* FastAPI
* Uvicorn

### Database

* PostgreSQL
* Neon PostgreSQL

### AI / ML

* NLP-based sentiment and emotion analysis
* DeepFace
* OpenCV
* AI-powered Wellness Chat

### Authentication & Security

* bcrypt password hashing
* JWT authentication
* OTP verification
* Environment variables / secrets

### Deployment / Access

* Google Colab
* Ngrok
* Streamlit

---

## 🔄 Application Workflow

```text
User Registration
       ↓
Email OTP Verification
       ↓
Secure Login
       ↓
Employee / Manager Dashboard
       ↓
┌─────────────────────────────────┐
│                                 │
▼                                 ▼
Mood Tracking              Journal Entry
│                                 │
│                                 ▼
│                          NLP Analysis
│                                 │
└──────────────┬──────────────────┘
               ▼
       Wellness Data Storage
               │
       ┌───────┼────────┐
       ▼       ▼        ▼
 Face Emotion  AI Chat  Weekly Report
 Analysis
       │       │        │
       └───────┼────────┘
               ▼
       Wellness Dashboard
               │
               ▼
        PDF Wellness Report
```

---

## 👥 User Roles

### 👤 Employee

Employees can:

* Create an account
* Login securely
* Record moods
* Write journal entries
* Analyze journal emotions
* Use Face-Based Emotion Analysis
* Use Wellness Chat
* View wellness dashboard
* Generate weekly wellness reports
* Download PDF reports

### 👨‍💼 Manager

Managers can:

* Login through the manager account
* View employee wellness information
* View latest employee mood information
* Analyze team mood trends
* View overall team-level wellness analytics

---

## 📊 Wellness Analytics

The system uses available wellness information to generate meaningful insights.

The weekly analysis considers information such as:

* Mood
* Emotion
* Stress
* Sleep
* Workload
* Journal activity
* Sentiment
* Emotion confidence

Missing information is handled separately rather than automatically treating it as zero.

---

## 🔒 Security

Security is an important part of the application.

The project uses:

* Password hashing
* OTP verification
* JWT authentication
* Secure session handling
* Environment variables for sensitive configuration
* PostgreSQL database storage

Sensitive credentials such as database passwords and Ngrok authentication tokens should be stored using environment variables or platform secrets instead of directly inside the source code.

---

## 📁 Project Structure

```text
AI-Based-Employee-Wellness-Management/
│
├── app.py
├── backend.py
├── db.py
├── requirements.txt
├── README.md
│
├── milestone1/
│   └── README.md
│
├── screenshots/
│   ├── login.png
│   ├── signup.png
│   ├── dashboard.png
│   ├── journal-analysis.png
│   ├── face-recognition.png
│   ├── wellness-chat.png
│   └── weekly-report.png
│
└── notebooks/
    └── Team-C.ipynb
```

> Update the folder/file names above if your actual GitHub repository structure is different.

---

## 🚀 Running the Project

### 1. Open the Google Colab Notebook

Open the project notebook in Google Colab.

### 2. Configure Secrets

Add required credentials such as:

```text
NGROK_AUTHTOKEN
```

and the required database/API secrets.

### 3. Run the Required Cells

Run the project setup cells and make sure the database and backend are running successfully.

### 4. Run Streamlit + Ngrok

Run the final **Streamlit + Ngrok** cell.

The cell will start the Streamlit application and create a public Ngrok URL.

Example:

```text
https://xxxx.ngrok-free.app
```

Use the **Ngrok public URL** to access the application.

Keep the **Colab runtime and Streamlit/Ngrok cell running** while using the application.

---

## 📸 Screenshots

The `screenshots` folder contains screenshots demonstrating the major features of the project, including:

* Login
* Signup
* Employee Home
* Mood Tracking
* Journal/NLP Analysis
* Face-Based Emotion Analysis
* Wellness Chat
* Dashboard
* Weekly Wellness Report
* PDF Report

---

## 🎓 Project Outcomes

The project successfully demonstrates how AI and data analytics can be used to support employee wellness monitoring.

It combines multiple sources of information such as **mood, journal text, facial emotion, stress, sleep and workload** to provide a more comprehensive wellness overview.

---

## 🔮 Future Enhancements

* More advanced emotion-recognition models.
* Improved personalization of wellness recommendations.
* Mobile application support.
* Real-time wellness notifications.
* More advanced employee/team analytics.
* Stronger privacy and consent controls.
* Improved AI wellness assistant.
* Integration with wearable devices for additional wellness data.

---

## 👩‍💻 Project

**Project Title:** AI-Based Employee Wellness Management

**Application:** MoodMentor

**Domain:** Artificial Intelligence / Machine Learning / NLP / Employee Wellness Analytics

**Platform:** Google Colab + Streamlit

---

## 🙏 Acknowledgement

This project was developed as part of our academic/project learning experience to demonstrate the practical application of **Artificial Intelligence, NLP, database management, web application development, and data analytics** in employee wellness management.
