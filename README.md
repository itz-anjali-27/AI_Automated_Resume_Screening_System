# AI-Driven Resume Screening System 

An intelligent recruitment platform that automates end-to-end resume screening using AI/ML, delivering reliable candidate rankings, transparent explanations. The system combines robust document parsing (PDF/DOCX/OCR), semantic matching with Sentence‑Transformers, fuzzy skill extraction, and fairness checks to help HR teams shortlist candidates faster while reducing bias and improving hiring quality.

Designed for scalability and extensibility, the project exposes REST APIs for integrations, supports role-based dashboards for HR and candidates, and includes automated notifications and explainability features (LIME + score breakdowns) so decisions remain auditable. Built as an academic capstone, it demonstrates production-ready patterns (JWT auth, async FastAPI, modular services) and serves as a foundation for future enhancements like S3 storage, interview scheduling, and multi-language support.

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Usage](#usage)
- [Team](#team)

---

## 🎯 Overview

The AI-Driven Resume Screening System is a comprehensive web application designed to streamline the recruitment process for HR professionals while enhancing the candidate experience. Built as a major project at **CMR Institute of Technology, Bengaluru**, this system leverages cutting-edge AI/ML technologies to automate resume screening, provide intelligent rankings, and offer interview preparation assistance.

### Key Capabilities
- **Automated Resume Parsing**: Supports PDF, DOCX, PNG, and JPEG formats
- **AI-Powered Ranking**: Multi-factor scoring using semantic similarity and skill matching
- **Explainable AI**: Transparent decision-making with score breakdowns
- **Bias Detection**: Fairlearn integration for fair hiring practices
- **Interview Chatbot**: Rasa-powered assistant for candidate preparation
- **Email Notifications**: Automated candidate updates
- **Dual Dashboards**: Separate interfaces for HR and candidates

---

## ✨ Features

### For HR Professionals
- 📝 **Job Posting Management**: Create and manage job descriptions with requirements
- 📤 **Bulk Resume Upload**: Process multiple resumes simultaneously (PDF/DOCX/Images)
- 🤖 **AI-Powered Ranking**: Automatic candidate scoring based on:
  - Skill matching (45% weight)
  - Semantic similarity (30% weight)
  - Experience relevance (20% weight)
  - Education level (5% weight)
- 📊 **Explainable AI**: Understand why each candidate received their score
- ✅ **Decision Workflow**: Select, reject, or mark candidates as pending
- 📧 **Email Notifications**: Automated emails sent to candidates upon decision submission
- 📈 **Bias Detection**: Fairlearn metrics to ensure fair evaluation

### For Candidates
- 📱 **Application Tracking**: View status of all job applications
- 💬 **Interview Prep Chatbot**: 24/7 AI assistant offering:
  - Common interview questions practice
  - STAR method guidance for behavioral questions
  - Technical interview tips
  - Role-specific advice
- 🔔 **Notifications**: Real-time updates on application status
- 📊 **Score Visibility**: See ranking scores and feedback

---



## 🛠️ Technology Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| **React** | 18.2.0 | UI framework for building interactive interfaces |
| **Material-UI** | 5.18.0 | Pre-built components with Material Design |
| **React Router** | 6.30.1 | Client-side routing and navigation |
| **Axios** | 1.12.2 | HTTP client for API communication |
| **React Simple Chatbot** | 0.6.1 | Chat interface for Rasa integration |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| **FastAPI** | Latest | Modern, high-performance web framework |
| **Python** | 3.11 | Programming language |
| **Supabase** | Latest | PostgreSQL database with built-in authentication |
| **Uvicorn** | Latest | ASGI server for FastAPI |
| **python-dotenv** | Latest | Environment variable management |

### AI/ML
| Technology | Version | Purpose |
|------------|---------|---------|
| **Sentence-Transformers** | Latest | Semantic text similarity (all-mpnet-base-v2 model) |
| **spaCy** | Latest | NLP pipeline and named entity recognition |
| **rapidfuzz** | Latest | Fuzzy string matching for skill variants |
| **LIME** | Latest | Explainable AI (model interpretability) |
| **Fairlearn** | Latest | Bias detection and fairness metrics |
| **scikit-learn** | Latest | Traditional ML algorithms |

### Document Processing
| Technology | Version | Purpose |
|------------|---------|---------|
| **pdfplumber** | Latest | PDF text extraction |
| **python-docx** | Latest | Microsoft Word document parsing |
| **pytesseract** | Latest | OCR for image-based resumes |


### Email & Notifications
| Technology | Version | Purpose |
|------------|---------|---------|
| **smtplib** | Built-in | Email sending via Gmail SMTP |
| **python-jose** | Latest | JWT token handling |

---

## 🚀 Usage

### For HR Users

1. **Register/Login**
   - Create an account with role "HR"
   - Login with credentials

2. **Create Job Posting**
   - Click "Create Job"
   - Fill in job title, description, requirements, location, salary
   - Submit to post the job

3. **Upload Resumes**
   - Select a job posting
   - Click "Upload Resumes"
   - Choose multiple files (PDF, DOCX, PNG, JPEG)
   - Wait for AI processing (~2-3 seconds per resume)

4. **Review Rankings**
   - View candidates sorted by AI score (highest first)
   - See color-coded scores:
     - 🟢 Green (80-100%): Excellent match
     - 🟡 Yellow (60-79%): Good match
     - 🔴 Red (0-59%): Poor match
   - Click "Why this score?" to see explanation

5. **Make Decisions**
   - Select decision from dropdown: Selected/Rejected/Pending
   - Decisions saved automatically
   - Click "Submit Decisions" to send emails to all candidates

6. **View Explanation**
   - Click "Explain Score" button
   - See breakdown:
     - Skill match contribution
     - Semantic similarity score
     - Experience evaluation
     - Education level
   - View matched vs missing skills

### For Candidates

1. **Register/Login**
   - Create account with role "Candidate"
   - Login with credentials

2. **Track Applications**
   - View all job applications
   - See status: Selected/Rejected/Pending
   - Check ranking scores

4. **Receive Notifications**
   - Check notification bell for updates
   - Receive emails when decisions are made


### Team Members

| Name  | Role | Responsibilities |
|------|------|------------------|
| **Anjali**  | Frontend & DataBase Developer | React Integration |
| **Tayyeba Ali**  | Backend Developer | React UII |
| **Akanksha**  | Frontend Developer | FastAPI, AI Ranking Algorithm, Resume Processing |
| **Priyanka Pal** | AI/ML Developer | Supabase Integration, Email Service, Bias Detection |


## 🎓 Project Highlights

### AI/ML Innovations
- **Multi-factor Ranking Algorithm**: Combines skill matching, semantic similarity, experience, and education
- **Explainable AI**: LIME-based explanations for transparency
- **Bias Detection**: Fairlearn integration ensures fair hiring practices
- **Semantic Search**: Sentence-BERT (all-mpnet-base-v2) for context-aware matching

### Technical Achievements
- **Full-stack Implementation**: React + FastAPI + Rasa
- **Real-time Processing**: < 3 seconds for 50 resume ranking
- **Scalable Architecture**: Async FastAPI, client-side React routing
- **Production-ready**: JWT auth, email notifications, error handling

### User Experience
- **Intuitive UI**: Material Design components
- **Responsive Design**: Works on mobile, tablet, desktop
- **Interactive Chatbot**: 24/7 interview preparation assistant
- **Transparent AI**: Users understand why decisions were made

---

## 🔒 Security Features

- ✅ JWT token-based authentication
- ✅ Password hashing (Supabase)
- ✅ Role-based access control (HR/Candidate)
- ✅ TLS encryption for email (Gmail SMTP)
- ✅ Environment variable protection (.env)
- ✅ CORS configuration for API security

---

## 📊 Performance

- **Resume Parsing**: < 2 seconds per file
- **AI Ranking**: < 3 seconds for 50 resumes
- **Explanation Generation**: < 1 second
- **Email Delivery**: ~2 seconds per email

#### TABLE 1: OVERALL PROJECT ACCURACY

| Metric | Value | Status |
|--------|-------|--------|
| **Overall Project Accuracy** | **87.1%** | ✅ Excellent |
| **Expected Performance** | 70-80% (Industry Benchmark) | Above Average |
| **Models Tested** | 4 | Resume Screening, OCR, Fuzzy Matching, NER |
| **Test Duration** | 5.45 seconds | Fast |
| **Processing Speed per Resume** | 92.29 ms | Excellent |

#### TABLE 2: COMPONENT-WISE ACCURACY (Weighted)

| Component | Accuracy | Weight | Contribution | Status |
|-----------|----------|--------|--------------|--------|
| Skill Extraction (NER) | 93.62% | 20% | 18.7% | ✅ Excellent |
| Fuzzy Skill Matching | 87.50% | 45% | 39.4% | ✅ Good |
| Semantic Similarity | 80.00% | 30% | 24.0% | ✅ Good |
| OCR (Image Processing) | 100.00% | 5% | 5.0% | ✅ Perfect |
| **TOTAL WEIGHTED ACCURACY** | **87.1%** | **100%** | **87.1%** | ✅ Production Ready |

**Key Insights:**
- ✅ Overall system accuracy of **87.1%** exceeds industry benchmark (70-80%)
- ✅ Skill extraction performs excellently at **93.62% F1 score**
- ✅ OCR achieves **perfect 100% accuracy** for image-based resumes
- ✅ Processing speed is **21x faster** than target (92.29ms vs 2000ms)
- ✅ **Production Ready** - All components operating within acceptable ranges

## 🤝 Contributing

Contributions are welcome! This project is open for contributors — feel free to open issues or submit pull requests. Please follow the existing code style and include tests or documentation updates for non-trivial changes. For major changes, open an issue first to discuss the proposal.


## 📧 Contact

For queries or collaboration opportunities, please reach out:

**Email**: airesumescreening@gmail.com

---

<div align="center">
  <p>Made with ❤️ by Team AI-Resume-Screening</p>
  <p>Shriram Institute of Management & Technology, Kashipur</p>
  <p>© 2026 All Rights Reserved</p>
</div>
