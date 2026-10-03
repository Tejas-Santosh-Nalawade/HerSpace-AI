# 🌸 HerSpace — Agentic AI Support Platform for Working Women in India

> **An intelligent, voice-enabled multi-agent system providing personalized support for wellness, career growth, financial planning, safety, and work-life balance.**

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-async-009688?logo=fastapi&logoColor=white)
![Groq](https://img.shields.io/badge/LLM-Groq_LLaMA_3.3_70B-F55036)
![Vercel](https://img.shields.io/badge/Frontend-Vercel-000000?logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Backend-Render-46E3B7?logo=render&logoColor=white)

---

## 🎯 Problem Statement

Working women in India face unique challenges that often go unaddressed:

- **🏢 Workplace Health**: Long sitting hours causing back pain, neck strain, and eye fatigue with limited access to immediate relief guidance
- **⚖️ Work-Life Balance**: Overwhelming responsibilities across career, family, and personal well-being with minimal time management support
- **🚀 Career Growth**: Limited access to personalized upskilling resources and career guidance tailored to the Indian job market
- **💰 Financial Stress**: Lack of financial literacy and budgeting support specific to Indian banking and savings systems
- **🛡️ Safety Concerns**: Need for trauma-informed support and actionable safety guidance in the Indian context
- **😔 Mental Wellness**: Stress, anxiety, and burnout with no immediate, judgment-free support available 24/7

**The Gap**: Existing solutions are either expensive counseling, impersonal chatbots, or fragmented apps that don't understand the complete picture of a working woman's life.

---

## 💡 Our Solution: HerSpace

HerSpace is not just another chatbot — it's an **agentic AI system** where five specialized AI agents work together to provide:

✨ **Personalized Support**: Each agent learns from your interactions and builds a memory of your preferences, challenges, and goals  
🎙️ **Voice-First Experience**: Real-time voice guidance with Indian female voice, interactive breathing exercises, and speaking avatar  
🤖 **Multi-Agent Intelligence**: Five specialized agents collaborate to provide comprehensive support across all life domains  
📊 **Smart Dashboard**: Personalized insights and recommendations powered by real agent memory, not static data  
🔒 **Privacy-First**: All conversations stored locally with JWT authentication and optional Google OAuth  
🌏 **India-Focused**: Culturally relevant advice, Indian job market integration, and Hinglish voice support  

---

## ✨ Key Features

### 🎙️ Voice-First Experience
- **Auto-Speaking Responses**: Bot messages automatically spoken with Indian female voice (`en-IN` priority)
- **ElevenLabs Premium TTS**: High-quality multilingual streaming via `eleven_multilingual_v2` model (supports Hinglish) through `/api/v2/voice-tts`
- **Interactive Voice Sessions**: Real-time guided breathing exercises with step-by-step countdown
- **Speaking Avatar**: Animated purple avatar with pulse effects and waveform bars that animate when the AI is speaking
- **Voice Speed Optimization**: 1.25× rate for responses, 1.4× for countdowns
- **Voice Controls**: Stop, pause, and restart voice playback at any time
- **Speech-to-Text**: Browser `SpeechRecognition` API for hands-free voice input

### 🤖 Agentic Intelligence
- **Multi-Agent Collaboration**: Top-2 scoring agents respond together on complex cross-domain queries
- **Vector Memory**: Each agent stores and recalls conversation history using lightweight hash-based embeddings
- **Intent Routing**: Regex + LLM-hybrid classification routes queries to the right specialist
- **Continuous Learning**: Agents improve recommendations based on past interactions
- **Dashboard Intelligence**: Personalized metrics derived from real agent memory, not hardcoded values

### 🔒 Security & Privacy
- **JWT Authentication**: Secure token-based auth (HS256, 7-day tokens)
- **Google OAuth**: One-click sign-in with Google account (server-side token verification)
- **Local Storage**: All user data stored in flat JSON files — no external database required
- **Password Hashing**: bcrypt encryption via passlib

### 📱 User Experience
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Dark/Light Mode**: System theme detection with manual override
- **Offline Fallback**: Graceful degradation (v2 → v1 → keyword-matched offline responses)
- **Search Integration**: Find courses and jobs directly in chat via DuckDuckGo

---

## 🤖 The 5 Specialized AI Agents

### 💪 FitHer — Your Wellness Coach
**Focus**: Physical & Mental Wellness

- Quick desk exercises (2–5 minutes)
- Posture correction guidance
- Interactive breathing sessions (Box Breathing, 4-7-8, Deep Breathing)
- Eye strain and screen fatigue relief
- Neck and shoulder tension relief with step-by-step voice guidance
- Stress management and mental wellness support
- Tracks activity/stress events to calculate a live Wellness Score (0–100)

**Example**: *"I have back pain from sitting all day"*  
→ FitHer provides immediate desk stretches with a voice-guided interactive session

---

### 📅 PlanPal — Your Time Management Partner
**Focus**: Work-Life Balance & Productivity

- Smart task prioritization using energy levels, not just deadlines
- Realistic time-blocking that accounts for Indian work culture (long commutes, family obligations, invisible labor)
- Family-work balance strategies sensitive to in-law dynamics and caregiving responsibilities
- Break reminders and weekly planning assistance
- Task completion ratio tracked and surfaced on the dashboard

**Example**: *"I can't balance work and family time"*  
→ PlanPal creates a practical schedule tailored to your real constraints

---

### 🛡️ SpeakUp — Your Safety Ally
**Focus**: Workplace Safety & Harassment Support

- Trauma-informed, judgment-free support for workplace harassment and hostile environments
- Practical guidance on the POSH Act (Prevention of Sexual Harassment) and your legal rights
- India-specific safety resources, NGO contacts, and helplines
- Step-by-step guidance on filing complaints and building documentation
- Emotional support and action planning for difficult workplace situations

**Example**: *"My manager is making me uncomfortable and I don't know what to do"*  
→ SpeakUp explains your rights under the POSH Act and helps you plan next steps

---

### 🚀 GrowthGuru — Your Career Accelerator
**Focus**: Career Growth & Upskilling

- Live job search from Indian job boards via DuckDuckGo integration (real-time results)
- Live course search for upskilling (Coursera, Udemy, NPTEL, etc.)
- Personalized career guidance based on your role and goals
- Interview preparation and salary negotiation coaching
- Resume review pointers and LinkedIn profile advice
- Industry trends for the Indian job market

**Example**: *"I want to transition from operations to data analytics"*  
→ GrowthGuru searches for live courses + jobs and builds a learning roadmap

---

### 💰 PaisaWise — Your Financial Guide
**Focus**: Personal Finance & Investment Literacy

- India-specific budgeting using the 50-30-20 rule calibrated to Indian salaries and taxes
- SIP (Systematic Investment Plan) and mutual fund guidance
- PPF, NPS, and tax-saving investment explanation
- Savings goals and emergency fund planning
- Financial literacy for beginners with culturally relevant examples
- Finance engagement score tracked on the dashboard

**Example**: *"How do I start investing on a ₹40,000/month salary?"*  
→ PaisaWise builds a step-by-step savings and SIP plan

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                           USER INTERFACE                                 │
│                    (React 19 + TypeScript + Vite)                       │
│                                                                          │
│  ┌──────────────────────────────────────────────────────────────────┐  │
│  │  🎙️ Voice Interface          📊 Dashboard         💬 Chat Panel  │  │
│  │  • TTS/STT (Indian voice)    • Agent Insights    • Multi-bot    │  │
│  │  • ElevenLabs streaming      • Memory Metrics    • History      │  │
│  │  • Interactive Sessions      • Recommendations   • Voice Mode   │  │
│  │  • Speaking Avatar           • Analytics         • Search       │  │
│  └──────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────┘
                                    ↕ HTTP/REST API
┌─────────────────────────────────────────────────────────────────────────┐
│                         AGENTIC ROUTER                                   │
│                        (Python FastAPI)                                  │
│                                                                          │
│  ┌──────────────────────────────────────────────────────────────────┐  │
│  │  Intent Classification → Route to Specialist Agent               │  │
│  │  Multi-Agent Collaboration → Top-2 Agents Respond                │  │
│  │  Dashboard Service → Aggregate Agent Intelligence                │  │
│  └──────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────┘
                                    ↕
┌─────────────────────────────────────────────────────────────────────────┐
│                         5 SPECIALIZED AGENTS                             │
│                                                                          │
│  💪 FitHer    📅 PlanPal    🛡️ SpeakUp    🚀 GrowthGuru    💰 PaisaWise  │
│  Wellness    Planner       Safety        Career           Finance       │
│  Exercises   Scheduling    POSH Act      Live Job Search  SIP/PPF       │
│  Breathing   Priorities    Helplines     Live Courses     Budgeting     │
│                                                                          │
│  Each agent has:                                                         │
│  ✓ Isolated vector memory (pickle-persisted)                            │
│  ✓ Specialist system prompt (India-aware persona)                       │
│  ✓ Live tools (search, wellness search, etc.)                           │
│  ✓ Dashboard metric calculator                                           │
└─────────────────────────────────────────────────────────────────────────┘
                                    ↕
┌─────────────────────────────────────────────────────────────────────────┐
│                         INFRASTRUCTURE                                   │
│                                                                          │
│  🧠 LLM: Groq (llama-3.3-70b-versatile, sub-second responses)          │
│  🎤 Voice: ElevenLabs eleven_multilingual_v2 (Hinglish support)        │
│  🔍 Search: DuckDuckGo (job and course search)                          │
│  💾 Storage: JSON files (users) + pickle files (agent memory)           │
│  🔐 Auth: JWT (HS256) + Google OAuth                                    │
│  📦 Memory: Hash-based embeddings, 64 dims, ~5MB (vs 400MB ML models)  │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 🧠 How Agents Work

### Example: "I need time management and exercise help"

**Step 1 — Router scores all agents**
```
⚙️  Keywords + LLM intent + memory match
    PlanPal:    95 ✅  Primary
    FitHer:     90 ✅  Collaborates
    GrowthGuru: 42 ❌  Skipped
    SpeakUp:    18 ❌  Skipped
    PaisaWise:  12 ❌  Skipped
```

**Step 2 — PlanPal (primary)**
```
📅  Recalls memory: "User struggles with mornings"
    Builds a realistic schedule: 6:30 AM → 8:00 AM
    Requests FitHer's input on exercise fit
```

**Step 3 — FitHer (collaborates)**
```
💪  Recalls memory: "User has lower back pain"
    Selects low-impact morning routine
    Offers to start an interactive voice session
```

**Step 4 — Merged response**
```
✨  "Here's your morning routine:
     6:30 AM - Wake up + hydrate
     6:45 AM - Gentle stretching for back (10 min)
     7:00 AM - Breathing exercise (5 min)
     7:30 AM - Start focused work block
     [▶ Start Guided Session]  [⏰ Set Reminder]"
```

### Agent Scoring System

```
┌──────────────────────────────────┐
│  How Router Scores (0–100)       │
├──────────────────────────────────┤
│  Keywords match:    30 points    │
│  LLM intent score:  40 points    │
│  Memory relevance:  30 points    │
│  ──────────────────────────────  │
│  Total:             100 points   │
│                                  │
│  ≥ 80 → Primary (responds)       │
│  60–79 → Collaborates            │
│  < 60 → Skipped                  │
└──────────────────────────────────┘
```

---

## 🧬 Vector Memory

Each agent maintains its own isolated vector memory store (pickle-persisted):

```
FITHER'S MEMORY:
─────────────────────────────────────────────────────
Memory 1: "back pain from sitting"   Vector: [0.21, 0.89, ...]
Memory 2: "prefers 10-min exercise"  Vector: [0.67, 0.12, ...]
Memory 3: "energetic in mornings"    Vector: [0.34, 0.78, ...]
─────────────────────────────────────────────────────

New Query: "I want to exercise"
Query Vector: [0.25, 0.85, 0.42, ...]

Similarity Match (cosine):
  Memory 1: 0.92 ✅  High match → context added to prompt
  Memory 2: 0.87 ✅  High match → context added to prompt
  Memory 3: 0.45 ❌  Low match → skipped

→ Agent recommends low-impact exercises for back pain
```

**Why hash-based embeddings instead of ML models?**
```
Traditional:  "back pain" → sentence-transformers (400MB) → 384 dims
Our approach: "back pain" → MD5 hash (5MB)             →  64 dims

✅ 98% less memory  |  ✅ 10× faster  |  ✅ Fits Render's 512MB free tier
```

---

## 📊 Dashboard Intelligence

All metrics are computed from real agent memory and interaction data — not hardcoded:

```
┌───────────────────────────────────────────────────────┐
│  📈 YOUR HERSPACE DASHBOARD                           │
├───────────────────────────────────────────────────────┤
│  Total Conversations: 47                              │
│  💪 FitHer: 12   📅 PlanPal: 8   🛡️ SpeakUp: 3       │
│  🚀 GrowthGuru: 15   💰 PaisaWise: 9                  │
│                                                       │
│  🎯 Top Topics (from your chats):                    │
│    1. time management — 8 mentions                   │
│    2. back pain — 6 mentions                         │
│    3. career growth — 5 mentions                     │
│                                                       │
│  💚 Wellness Score: 72/100                           │
│     Based on FitHer activity in last 7 days          │
│                                                       │
│  💡 Recommendations:                                 │
│    • Haven't exercised in 3 days                    │
│    • 2 career resources waiting                     │
│    • Budget review due                              │
└───────────────────────────────────────────────────────┘

✅ Derived from: real chats + agent memories + activity patterns
❌ NOT from: hardcoded values or fake numbers
```

---

## 📁 Project Structure

```
FULL PRODUCT WOMEN/
├── frontend/                      # Frontend (React 19 + TypeScript + Vite)
│   ├── src/
│   │   ├── components/
│   │   │   ├── chat-panel.tsx           # Main chat UI with voice output
│   │   │   ├── dashboard.tsx            # Chat shell with bot selector
│   │   │   ├── personalized-dashboard.tsx # Landing dashboard (metrics)
│   │   │   ├── interactive-voice-guide.tsx # Real-time breathing sessions
│   │   │   ├── speaking-avatar.tsx       # Animated speaking avatar
│   │   │   ├── voice-avatar.tsx          # Avatar with waveform bars
│   │   │   ├── auth-form.tsx             # Login / Register form
│   │   │   ├── agentic-dashboard.tsx     # Agent metrics view
│   │   │   └── ui/                       # Radix UI / Shadcn components
│   │   ├── lib/
│   │   │   ├── api.ts                   # All API calls + auth token management
│   │   │   ├── voice-agent.ts           # TTS/STT logic, markdown stripping
│   │   │   ├── guided-sessions.ts       # Breathing/exercise session scripts
│   │   │   ├── voice-instructions.ts    # Voice session instruction content
│   │   │   └── analytics-tracker.ts     # Client-side usage tracking
│   │   ├── pages/
│   │   │   ├── Home.tsx                 # Main app shell
│   │   │   ├── Auth.tsx                 # Authentication page
│   │   │   └── Analytics.tsx            # Per-bot session analytics
│   │   └── hooks/
│   │       ├── use-mobile.ts
│   │       └── use-toast.ts
│   ├── public/
│   ├── vercel.json                # Vercel deployment config
│   └── package.json
│
├── backend/                       # Backend (Python 3.11 + FastAPI)
│   ├── main.py                    # FastAPI app — all routes (v1, v2, auth)
│   ├── auth.py                    # JWT + Google OAuth authentication
│   ├── bots.py                    # Bot personas and system prompts
│   ├── search_utils.py            # DuckDuckGo job/course search
│   ├── elevenlabs_service.py      # ElevenLabs streaming TTS proxy
│   ├── agents/
│   │   ├── base_agent.py          # Base class: memory + LLM generation
│   │   ├── agent_manager.py       # Manages all agents
│   │   ├── wellness_agent.py      # FitHer
│   │   ├── planner_agent.py       # PlanPal
│   │   ├── safety_agent.py        # SpeakUp
│   │   ├── career_agent.py        # GrowthGuru (live search)
│   │   └── finance_agent.py       # PaisaWise
│   ├── memory/
│   │   ├── embedding.py           # Hash-based embedding (MD5 → 64 dims)
│   │   └── vector_store.py        # Cosine-similarity vector memory
│   ├── orchestrator/
│   │   ├── router.py              # Intent classification + agent routing
│   │   └── dashboard.py           # Aggregate metrics from all agents
│   ├── storage/
│   │   └── users.json             # User database (flat file)
│   ├── requirements.txt           # Full dependencies
│   ├── requirements-light.txt     # Render-optimized (512MB) deps
│   └── render.yaml                # Render deployment config
│
├── architecture/                  # Design documentation (16 files)
│   ├── AGENTIC_ARCHITECTURE.md
│   ├── AUTH_SYSTEM_COMPLETE.md
│   ├── GOOGLE_OAUTH_SETUP.md
│   └── DEMO_CHECKLIST.md
│
├── doc/                           # Product documents
│   └── HerSpace_Product_Document.md
│
├── testing/                       # Validation scripts and test data
│   ├── feasibility_validation.py
│   └── live_backend_test.py
│
└── README.md
```

---

## 🚀 Quick Start (Development)

### Prerequisites

- **Node.js** 18+
- **Python** 3.10+
- **Groq API Key** — free at [console.groq.com](https://console.groq.com)
- *(Optional)* **ElevenLabs API Key** — for premium TTS with Hinglish support

### Backend

```bash
cd backend
python -m venv venv

# Activate (Mac/Linux)
source venv/bin/activate
# Activate (Windows)
.\venv\Scripts\Activate.ps1

pip install -r requirements.txt
cp .env.example .env          # then fill in your keys
uvicorn main:app --reload --port 8000
```

### Frontend

```bash
cd frontend
npm install
npm run dev                   # starts on http://localhost:5173
```

> **Windows tip**: If Python isn't in PATH, use `py -m venv venv` and `py -m pip install -r requirements.txt`.

### Local URLs

| Service  | URL                          | Description           |
|----------|------------------------------|-----------------------|
| Frontend | http://localhost:5173        | Main web application  |
| Backend  | http://localhost:8000        | FastAPI server        |
| API Docs | http://localhost:8000/docs   | Swagger UI            |

---

## 🔐 Environment Variables

### Backend (`backend/.env`)

```env
GROQ_API_KEY=gsk_your_groq_api_key_here
JWT_SECRET=your_secure_random_secret_minimum_32_chars
GOOGLE_CLIENT_ID=your_google_client_id.apps.googleusercontent.com
GOOGLE_CLIENT_SECRET=your_google_client_secret
ELEVENLABS_API_KEY=your_elevenlabs_api_key   # optional, for premium TTS
```

### Frontend (`frontend/.env.local`)

```env
VITE_API_URL=http://localhost:8000
```

---

## 🔧 API Endpoints

### Authentication

```http
POST /api/auth/register
Content-Type: application/json

{ "email": "user@example.com", "password": "securepass123", "full_name": "Jane Doe" }
```

```http
POST /api/auth/login
Content-Type: application/json

{ "email": "user@example.com", "password": "securepass123" }
```

```http
POST /api/auth/social
Content-Type: application/json

{ "token": "<google_id_token>" }
```

### v1 — Legacy (no memory)

```http
GET  /api/v1/bots                        # list all 5 bots

POST /api/v1/chat
{ "bot_id": "wellness", "message": "I have back pain", "history": [] }
```

### v2 — Agentic (memory-enabled, recommended)

```http
# Chat directly with a specific agent (stores memory)
POST /api/v2/agent/{agent_name}
Authorization: Bearer <jwt_token>
{ "message": "Help me with time management" }

# Auto-routing: top-2 agents respond
POST /api/v2/agentic-chat
Authorization: Bearer <jwt_token>
{ "message": "I need help with my back pain and work schedule" }

# Dashboard metrics from all agents
GET /api/v2/dashboard
Authorization: Bearer <jwt_token>

# Personalized time-of-day greeting
GET /api/v2/greeting
Authorization: Bearer <jwt_token>

# Per-agent memory summary
GET /api/v2/agent/{agent_name}/summary
Authorization: Bearer <jwt_token>

# ElevenLabs TTS streaming (Hinglish support)
POST /api/v2/voice-tts
Authorization: Bearer <jwt_token>
{ "text": "Your wellness score improved!", "voice_id": "optional" }
```

---

## 🚢 Deployment

### Recommended Setup
- **Frontend**: Vercel (free tier, auto-deploys from GitHub)
- **Backend**: Render (free tier, 512MB RAM — optimized for this)

### Backend on Render

1. Push to GitHub
2. Create a **Web Service** on [render.com](https://render.com)
3. Set root directory: `backend`
4. Build command: `pip install -r requirements-light.txt`
5. Start command: `uvicorn main:app --host 0.0.0.0 --port $PORT --workers 1`
6. Add env vars: `GROQ_API_KEY`, `JWT_SECRET`, `GOOGLE_CLIENT_ID`, `GOOGLE_CLIENT_SECRET`

### Frontend on Vercel

1. Import the GitHub repo on [vercel.com](https://vercel.com)
2. Set root directory: `frontend`
3. Add env var: `VITE_API_URL=https://your-render-service.onrender.com`
4. Deploy — Vercel handles the rest via `vercel.json`

**Memory usage on free tier**: ~80–100 MB (well under the 512 MB Render limit, thanks to hash-based embeddings instead of ML models).

---

## 📝 Tech Stack

### Frontend
| Technology | Version | Purpose |
|---|---|---|
| React + TypeScript | 19 / 5.9 | UI framework |
| Vite | 7.2.4 | Build tool (port 5173) |
| Tailwind CSS v4 | — | Styling |
| Radix UI (40+ components) | — | Accessible UI primitives |
| React Router DOM | v7 | Client-side routing |
| Recharts | — | Analytics charts |
| Web Speech API | browser-native | TTS / STT |
| @react-oauth/google | — | Google OAuth sign-in |
| next-themes | — | Dark/light mode |

### Backend
| Technology | Version | Purpose |
|---|---|---|
| Python + FastAPI | 3.11 | Async REST API (port 8000) |
| Groq API | llama-3.3-70b-versatile | LLM inference |
| ElevenLabs | eleven_multilingual_v2 | Premium TTS (Hinglish) |
| PyJWT + bcrypt | — | Auth + password hashing |
| google-auth | — | Google OAuth token verification |
| DuckDuckGo Search | — | Live job / course search |
| NumPy | — | Vector math for memory |

### Infrastructure
| Service | Purpose |
|---|---|
| Vercel | Frontend hosting (free tier) |
| Render | Backend hosting (512MB free tier) |
| GitHub | Source control + CI/CD |

---

## 🎯 Future Roadmap

### Phase 1 ✅ (Current)
- [x] 5 specialized AI agents with vector memory
- [x] Voice-first interface with Indian female voice
- [x] ElevenLabs Hinglish TTS
- [x] Interactive guided breathing and exercise sessions
- [x] JWT + Google OAuth authentication
- [x] Dashboard with live agent intelligence
- [x] Production deployment (Vercel + Render)

### Phase 2 🚧 (Planned)
- [ ] Regional language support (Hindi, Tamil, Bengali)
- [ ] WhatsApp integration for reminders and check-ins
- [ ] Mobile app (React Native)
- [ ] Google Calendar integration
- [ ] Habit tracking and streaks
- [ ] Anonymous community forums

### Phase 3 🔮 (Future)
- [ ] Video-based wellness sessions
- [ ] AI-powered resume builder
- [ ] Mock interview practice with feedback
- [ ] Financial planning with bank API integration
- [ ] Telemedicine integration
- [ ] Corporate wellness B2B offering

---

## 🏆 Hackathon Highlights

### Innovation
✨ **Not just a chatbot**: Multi-agent system with real memory and agent collaboration  
✨ **Voice-first with Hinglish**: ElevenLabs multilingual TTS + browser STT, Indian voice priority  
✨ **India-focused**: Culturally relevant advice, POSH Act knowledge, Indian financial instruments  
✨ **Privacy-first**: No external database — all data stored in local flat files  
✨ **Memory-optimized**: Runs on free tier (512 MB) using hash-based embeddings  

### Technical Excellence
🔧 **Agentic Architecture**: 5 autonomous agents with isolated vector memory  
🔧 **Hybrid Intent Routing**: Regex keywords + LLM intent scoring + memory relevance (100-pt scale)  
🔧 **Lightweight Embeddings**: MD5 hash-based, 64 dimensions, 5 MB vs 400 MB for ML models  
🔧 **Voice UX**: Speaking avatar, auto-speak, interactive sessions, ElevenLabs streaming  
🔧 **Production-Ready**: Deployed on Vercel + Render with continuous deployment  

### Real-World Impact
💡 **Accessibility**: 24/7 support — no appointments, no waitlists  
💡 **Affordability**: Free for users, minimal infrastructure cost  
💡 **Holistic**: Addresses wellness, career, finance, safety, and work-life balance together  
💡 **Inclusivity**: Designed around the specific challenges of working women in India  

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes and test thoroughly (frontend + backend)
4. Commit: `git commit -m "feat: add amazing feature"`
5. Push: `git push origin feature/amazing-feature`
6. Open a Pull Request

**Development guidelines**:
- Test voice features in Chrome or Edge (best Web Speech API support)
- Keep backend dependencies light — Render's free tier has a 512 MB RAM limit
- Run `cd frontend && npm run lint` before committing frontend changes

---

## 🙏 Acknowledgments

- **Groq** — lightning-fast LLaMA inference
- **ElevenLabs** — multilingual voice synthesis with Hinglish support
- **Shadcn/ui + Radix UI** — beautiful, accessible components
- **DuckDuckGo** — privacy-respecting search API
- **Vercel & Render** — generous free tiers that made deployment possible
- **Working Women of India** — for inspiring this project

---

## 📄 License

Part of the TIAA GC Hackathon — Women Health Enhancer category.

---

<div align="center">

### Built with ❤️ for working women in India

**HerSpace** — *Your AI companion for wellness, growth, and balance*

[📚 Architecture Docs](./architecture) · [🔧 Backend API](http://localhost:8000/docs)

---

*"Empowering every working woman with personalized AI support — because you deserve it."*

</div>
