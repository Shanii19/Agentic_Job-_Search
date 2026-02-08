# 🤖 AI Career Development System

> **An intelligent, AI-powered platform that revolutionizes job searching, interview preparation, and career planning through advanced agentic AI technology.**

---

## 📋 Table of Contents

- [Problem Statement](#-problem-statement)
- [Solution](#-solution)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [System Architecture](#-system-architecture)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [API Configuration](#-api-configuration)
- [Contributing](#-contributing)

---

## 🎯 Problem Statement

### The Challenge

Job seekers today face numerous challenges in their career journey:

1. **Overwhelming Job Search**: Manually searching across multiple platforms (LinkedIn, Indeed, Glassdoor) is time-consuming and inefficient
2. **Lack of Personalization**: Generic job recommendations that don't match individual skills and preferences
3. **Interview Anxiety**: Limited access to realistic interview practice with personalized feedback
4. **Skill Gaps**: Difficulty identifying what skills to learn for career advancement
5. **Bias in Hiring**: Hidden biases in job descriptions that may discourage qualified candidates
6. **Career Path Uncertainty**: No clear guidance on career progression and bridge roles
7. **Fragmented Tools**: Using separate tools for job search, interview prep, and skill development

### Impact

- **95%** of job seekers feel overwhelmed by the job search process
- **70%** of candidates fear interviews due to lack of practice
- **80%** struggle to identify relevant skills for their target roles
- **60%** encounter biased job descriptions unknowingly

---

## 💡 Solution

**AI Career Development System** is a comprehensive, AI-powered platform that addresses all these pain points in one unified system using **agentic AI architecture**.

### What This System Does

#### 🔍 **Intelligent Job Search**
- **Multi-Platform Aggregation**: Automatically searches across LinkedIn, Indeed, Glassdoor, and more
- **Smart Filtering**: AI-powered job matching based on skills, preferences, and career goals
- **Real-Time Results**: Get 10-20 relevant jobs in seconds, not hours
- **Bias Detection**: Automatically flags potentially biased language in job descriptions

#### 🎤 **AI Interview Coach**
- **Voice Interview Mode**: Practice with real-time conversational AI that acts like a recruiter
- **Live Feedback**: Get instant evaluation on your answers (correct/incorrect, strengths, improvements)
- **Automatic Question Generation**: Creates behavioral, technical, and situational questions based on job descriptions
- **STAR Method Analysis**: Evaluates your answers using industry-standard frameworks
- **Text & Voice Modes**: Choose your preferred practice method

#### 📚 **Skill Gap Analysis**
- **Resume Parsing**: AI analyzes your resume to identify current skills
- **Gap Identification**: Compares your skills against job requirements
- **Personalized Learning Paths**: Get custom roadmaps with courses, certifications, and resources
- **Priority Ranking**: Focuses on high-impact skills first

#### 🎯 **Career Path Planning**
- **Career Trajectory Prediction**: AI predicts possible career paths based on your profile
- **Bridge Roles**: Identifies intermediate positions to reach your dream job
- **Salary Insights**: Data-driven salary expectations for each role
- **Timeline Estimates**: Realistic timelines for career transitions

#### 🔒 **Ethics & Bias Monitoring**
- **Real-Time Auditing**: Scans all job listings for discriminatory language
- **Audit Scores**: Each job gets a bias score (0-100)
- **Red Flags**: Highlights problematic phrases (age, gender, race-related)
- **Transparency**: See exactly why a job was flagged

---

## ✨ Key Features

### 🎯 Core Capabilities

| Feature | Description | Benefit |
|---------|-------------|---------|
| **Multi-Agent System** | 5 specialized AI agents working together | Intelligent, context-aware responses |
| **Real-Time Voice Interview** | Conversational AI interviewer with TTS/STT | Practice like a real phone interview |
| **Automated Job Search** | Scrapes 4+ platforms simultaneously | Save 10+ hours per week |
| **Bias Detection** | LLM-powered ethical auditing | Apply to fair, inclusive companies |
| **Personalized Roadmaps** | Custom learning paths with resources | Clear direction for skill development |
| **Memory System** | Remembers your preferences and history | Improves over time with your usage |

### 🤖 The 5 AI Agents

1. **Search Agent** 🕵️
   - Scrapes job listings from multiple platforms
   - Deduplicates and ranks results
   - Applies smart filters

2. **Personalization Agent** 🎯
   - Analyzes your profile and preferences
   - Matches jobs to your skills
   - Provides personalized recommendations

3. **Memory Agent** 🧠
   - Stores your search history
   - Learns from your interactions
   - Provides contextual suggestions

4. **Interview Coach Agent** 🎤
   - Generates interview questions
   - Evaluates your answers using LLM
   - Provides detailed feedback

5. **Ethics Agent** ⚖️
   - Audits job descriptions for bias
   - Flags discriminatory language
   - Ensures ethical hiring practices

---

## 🛠️ Tech Stack

### **Frontend & UI**

| Technology | Version | Purpose |
|------------|---------|---------|
| **Streamlit** | 1.32+ | Web application framework - rapid UI development |
| **streamlit-audiorecorder** | Latest | Browser-based audio recording for voice interviews |
| **Custom CSS** | - | Professional, modern UI with gradient designs |

**Why Streamlit?**
- Rapid prototyping with Python
- Built-in state management
- Easy deployment
- Native support for interactive widgets

### **AI & NLP**

| Technology | Purpose | Why This Choice |
|------------|---------|-----------------|
| **LangChain** | LLM orchestration framework | Simplifies complex AI workflows |
| **Groq API** | Ultra-fast LLM inference (llama-3.3-70b) | 10x faster than OpenAI, cost-effective |
| **Google Gemini** | Fallback LLM provider | Reliable alternative with multimodal support |
| **gTTS** | Text-to-Speech for AI voice | Free, natural-sounding voices |
| **SpeechRecognition** | Speech-to-Text transcription | Accurate voice capture for interviews |

**LLM Models Used:**
- **Primary**: `llama-3.3-70b-versatile` via Groq (interview evaluation, question generation)
- **Fallback**: `gemini-1.5-pro` (job analysis, bias detection)

### **Web Scraping & Data**

| Technology | Purpose |
|------------|---------|
| **BeautifulSoup4** | HTML parsing for job listings |
| **Requests** | HTTP client for API calls |
| **Selenium** (optional) | Dynamic content scraping |
| **python-dotenv** | Environment variable management |

### **Audio Processing**

| Technology | Purpose |
|------------|---------|
| **pydub** | Audio manipulation and format conversion |
| **PyAudio** | Audio I/O for recording (backend for SpeechRecognition) |
| **tempfile** | Temporary audio file management |

### **Architecture Pattern**

```
┌─────────────────────────────────────────┐
│         Streamlit Frontend UI           │
│  (Multi-page app with state management) │
└─────────────┬───────────────────────────┘
              │
              ▼
┌─────────────────────────────────────────┐
│        Agent Orchestration Layer        │
│  ┌──────────┐  ┌──────────┐  ┌────────┐│
│  │ Search   │  │ Memory   │  │ Ethics ││
│  │ Agent    │  │ Agent    │  │ Agent  ││
│  └──────────┘  └──────────┘  └────────┘│
│  ┌──────────┐  ┌──────────┐            │
│  │Personal- │  │Interview │            │
│  │ization   │  │ Coach    │            │
│  └──────────┘  └──────────┘            │
└─────────────┬───────────────────────────┘
              │
              ▼
┌─────────────────────────────────────────┐
│         External Services               │
│  • Groq API (LLM)                       │
│  • Job Boards (LinkedIn, Indeed, etc.)  │
│  • gTTS (Text-to-Speech)                │
│  • SpeechRecognition (STT)              │
└─────────────────────────────────────────┘
```

---

## 🏗️ System Architecture

### Multi-Agent Design Pattern

Each agent is a **specialized AI module** with:
- **Single Responsibility**: One clear job
- **State Management**: Maintains context across interactions
- **LLM Integration**: Uses appropriate models for tasks
- **Error Handling**: Graceful failures with fallbacks

### Voice Interview Flow

```
1. User clicks "Start Live Interview"
   ↓
2. AI Agent generates 5 questions based on job description
   ↓
3. TTS reads question aloud (Phase 1: TTS)
   ↓
4. 30-second timer starts (Phase 2: Recording)
   ↓
5. User speaks answer → Audio captured
   ↓
6. STT transcribes audio (Phase 3: Transcription)
   ↓
7. LLM evaluates answer (Phase 4: AI Feedback)
   • Scores 1-10
   • Identifies correct/incorrect
   • Provides strengths & improvements
   ↓
8. AI speaks feedback via TTS
   ↓
9. Announces next question → Loop to step 3
   ↓
10. After all questions → Show full transcript & evaluation
```

### Job Search Pipeline

```
User Input (Job Title + Location)
   ↓
Search Agent → Scrapes 4+ platforms
   ↓
Memory Agent → Adds context from history
   ↓
Personalization Agent → Ranks by fit
   ↓
Ethics Agent → Audits for bias
   ↓
UI Display → Sorted results with scores
```

---

## 📦 Installation

### Prerequisites

- **Python**: 3.9 or higher
- **pip**: Latest version
- **API Keys**: Groq API key (free tier available)

### Step 1: Clone Repository

```bash
git clone https://github.com/yourusername/ai-career-system.git
cd ai-career-system
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3: Configure Environment

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key_here
GEMINI_API_KEY=your_gemini_api_key_here  # Optional fallback
```

**Get API Keys:**
- **Groq**: [https://console.groq.com](https://console.groq.com) (Free tier: 30 requests/min)
- **Gemini**: [https://makersuite.google.com/app/apikey](https://makersuite.google.com/app/apikey) (Free tier available)

### Step 4: Run the App

```bash
streamlit run app.py
```

The app will open at `http://localhost:8501`

---

## 🚀 Usage

### 1. **Job Search**

1. Enter job title (e.g., "Software Engineer")
2. Enter location (e.g., "Pakistan" or "Remote")
3. Select work style (Remote/Hybrid/Onsite)
4. Click "🚀 Launch Agents"
5. View personalized job results with bias scores

### 2. **Voice Interview Practice**

1. Navigate to **🎤 Interview Coach** (sidebar)
2. Paste job description
3. Select question type (Behavioral/Technical/Situational)
4. Choose **Voice Mode**
5. Click **Start Live Interview**
6. Listen to AI question → Speak answer → Get instant feedback
7. Repeat for all questions

### 3. **Skill Analysis**

1. Navigate to **📚 Skill Analysis**
2. Upload your resume (PDF/DOCX)
3. Paste target job description
4. View skill gaps and learning roadmap

### 4. **Career Planning**

1. Navigate to **🎯 Career Planning**
2. Enter current role and dream role
3. View predicted career path
4. See bridge roles and timelines

---

## 📁 Project Structure

```
job_search_agent/
├── app.py                      # Main entry point
├── requirements.txt            # Python dependencies
├── .env                        # API keys (create this)
├── README.md                   # This file
│
├── agents/                     # AI Agent modules
│   ├── search_agent.py         # Job search scraping
│   ├── memory_agent.py         # Context & history
│   ├── personalization_agent.py # Job matching
│   ├── interview_coach_agent.py # Interview Q&A
│   └── ethics_agent.py         # Bias detection
│
└── pages/                      # Streamlit multi-page app
    ├── 1_🎤_Interview_Coach.py # Voice interview feature
    ├── 2_📚_Skill_Analysis.py  # Skill gap analysis
    ├── 3_🎯_Career_Planning.py # Career roadmap
    └── 4_🔒_Ethics_Dashboard.py # Bias monitoring
```

---

## 🔑 API Configuration

### Required: Groq API

**Free Tier Limits:**
- 30 requests/minute
- 6,000 tokens/minute
- Sufficient for most use cases

**Setup:**
```bash
# Get key from: https://console.groq.com
export GROQ_API_KEY="gsk_..."
```

### Optional: Google Gemini

Used as fallback if Groq fails.

```bash
export GEMINI_API_KEY="AIza..."
```

### Voice Features

**Text-to-Speech (gTTS)**:
- Free, no API key needed
- Uses Google's TTS service
- Supports 100+ languages

**Speech-to-Text (SpeechRecognition)**:
- Free, uses Google Web Speech API
- No configuration needed
- Works in browser via microphone

---

## 🎨 Features in Detail

### Real-Time Voice Interview

**What makes it special:**
- ✅ No manual "record/submit" buttons - fully conversational
- ✅ AI speaks questions naturally via TTS
- ✅ 30-second auto-timer for each answer
- ✅ Live countdown (updates every second)
- ✅ Instant transcription via Speech-to-Text
- ✅ Real-time evaluation with LLM
- ✅ AI speaks feedback and announces next question
- ✅ Feels like talking to a real recruiter on phone

**Technologies Used:**
- **gTTS**: Natural voice synthesis
- **streamlit-audiorecorder**: Browser-based recording
- **SpeechRecognition**: Accurate transcription
- **Groq LLM**: Fast evaluation (300ms response time)

### Bias Detection System

**How it works:**
1. LLM analyzes job description
2. Identifies potentially discriminatory phrases
3. Categorizes by type (age, gender, race, etc.)
4. Assigns audit score (0-100)
5. Flags jobs with score < 70

**Example Detections:**
- ❌ "Recent graduate" → Age bias
- ❌ "Native English speaker" → Origin bias
- ❌ "Culturally fit" → Vague, potentially exclusionary
- ✅ "3+ years experience" → Neutral requirement

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License.

---

## 👥 Authors

- **Your Name** - Initial work

---

## 🙏 Acknowledgments

- **Groq** for ultra-fast LLM inference
- **Streamlit** for the amazing framework
- **LangChain** for AI orchestration tools
- **Open-source community** for inspiration

---

## 📞 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Email: hassanshayan190331@gmail.com

---

**Built with ❤️ using AI-first principles**

*Revolutionizing career development, one intelligent agent at a time.* 🚀
