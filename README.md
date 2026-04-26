# 🗂️ DataNexus AI Chat

**An AI-powered Data Catalog Chat Application built with OpenMetadata**

![DataNexus AI Chat](favicon.png)

> Connect. Analyze. Govern. Your data, intelligently.

---

## 🎯 Overview

**DataNexus AI Chat** is an intelligent conversational assistant for data governance and catalog management. Built during the **WeMakeDevs × OpenMetadata "Back to the Metadata" Hackathon**, it combines real-time data catalog access with AI-powered insights to help teams understand, manage, and govern their data assets.

### Key Differentiators
- 🤖 **AI-Powered Conversations** — Ask questions in plain English, get instant answers about your data
- 🔗 **Real-Time Lineage Visualization** — Trace data flow from source to destination
- 🔒 **PII Detection** — Automatically identify and flag personally identifiable information
- ✅ **Quality Monitoring** — Real-time data quality metrics and alerts
- ⏱️ **Time Travel** — Track data changes and schema evolution
- 🎨 **Beautiful Dark UI** — Modern, responsive design with particle effects

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────┐
│                   DataNexus AI Chat                      │
├─────────────────────────────────────────────────────────┤
│                                                           │
│  Frontend (index.html)                                   │
│  ├── Vanilla JavaScript (no frameworks)                  │
│  ├── Particle animation background (Canvas API)          │
│  ├── Real-time API integration                           │
│  └── Beautiful dark UI with gradient effects             │
│                                                           │
│  Backend (backend.py - FastAPI)                          │
│  ├── OpenMetadata API integration                        │
│  ├── Groq AI chat engine (LLaMA 3.1 8B)                 │
│  ├── Token caching & optimization                        │
│  └── Async request handling (httpx)                      │
│                                                           │
│  Data Layer (Docker Containers)                          │
│  ├── OpenMetadata Server                                 │
│  ├── MySQL Database                                      │
│  ├── Elasticsearch                                       │
│  └── Ingestion Pipeline                                  │
│                                                           │
└─────────────────────────────────────────────────────────┘
```

---

## ✨ Features

### 1. **Intelligent Chat Interface**
- Ask questions about your data in natural language
- AI-powered responses using Groq's LLaMA 3.1 model
- Real-time integration with OpenMetadata
- Context-aware answers based on actual metadata

### 2. **Data Catalog Search**
- Search tables, pipelines, and datasets instantly
- Real metadata from your OpenMetadata instance
- Owner and tag information
- Description and documentation included

### 3. **Lineage Visualization**
- View data flow relationships
- Trace upstream and downstream dependencies
- Identify data sources and consumers
- Beautiful flow diagrams

### 4. **PII Detection**
- Automatic scanning for personally identifiable information
- Highlights sensitive data tables
- Risk assessment and recommendations
- AI-powered analysis of sensitive columns

### 5. **Data Quality Monitoring**
- Real-time quality metrics from OpenMetadata
- Active alerts for data issues
- Quality score tracking
- Test case results with status indicators

### 6. **Time Travel History**
- Track schema changes over time
- View data modification history
- Understand data evolution
- Timeline visualization of changes

### 7. **System Health Dashboard**
- Real-time operational status
- Table and pipeline counts
- System metrics at a glance
- Green indicator for system health

---

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Python 3.10+
- Groq API Key (free at [console.groq.com](https://console.groq.com))
- Git

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/ganeshark04/datanexus-ai-chat
cd datanexus-ai-chat
```

2. **Create `.env` file**
```bash
echo "GROQ_API_KEY=your_groq_api_key_here" > .env
```

Get your free API key from: https://console.groq.com

3. **Start Docker containers**
```bash
docker compose up --detach
```

Wait 2-3 minutes for OpenMetadata to be fully ready...

4. **Install Python dependencies**
```bash
pip install -r requirements.txt
```

5. **Run the backend**
```bash
python backend.py
```

The app will automatically open in your browser! 🌐

---

## 📋 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Health check |
| `/test` | GET | Connection test |
| `/search?query=X` | GET | Search data catalog |
| `/lineage?table=X` | GET | Get data lineage |
| `/quality` | GET | Data quality metrics |
| `/pii` | GET | PII detection results |
| `/tables` | GET | List all tables |
| `/chat` | POST | AI chat endpoint |
| `/impact?table=X` | GET | Impact analysis |
| `/health?table=X` | GET | Data health score |

---

## 💻 Technology Stack

### Frontend
- **Vanilla JavaScript** (no framework dependencies)
- **HTML5 & CSS3** (modern, responsive design)
- **Canvas API** (particle animation effects)
- **Fetch API** (real-time data fetching)

### Backend
- **FastAPI** (modern async Python framework)
- **Python 3.10+**
- **httpx** (async HTTP client with connection pooling)
- **python-dotenv** (environment management)

### AI & Data
- **Groq API** (LLaMA 3.1 8B Instant model)
- **OpenMetadata** (data catalog & governance)
- **Docker** (containerization)

### Databases
- **MySQL** (OpenMetadata store)
- **Elasticsearch** (search & indexing)

---

## 🤖 AI Tools Used

This project was developed with assistance from AI tools:

- **Claude AI** - Used for code assistance, architecture design, UI/UX design, documentation, and development guidance
- **Groq AI (LLaMA 3.1)** - Integrated as the conversational engine in the application

**Disclosure:** We used AI tools to accelerate development during the hackathon. All code is original, properly attributed, and open source. The AI tools helped with scaffolding and guidance, but all logic, integration, and customization is our own work.

This reflects the future of development - leveraging AI tools for efficiency while maintaining transparency and quality.

---

## 🎯 Hackathon Information

**Event:** WeMakeDevs × OpenMetadata "Back to the Metadata" Hackathon  
**Dates:** April 17–26, 2026  
**Prize Pool:** $7,000  
**Track:** T-01 MCP Ecosystem & AI Agents  
**Issue:** #26608 — Conversational Data Catalog Chat App  
**Repository:** https://github.com/OpenMetadata/OpenMetadata/issues/26608  
**Registration:** https://forms.gle/gogMB2AjCbeFQdZZ8

---

## 👥 Team

| Name | Role | GitHub |
|------|------|--------|
| **Gagan Rao K** | Full Stack Developer & Lead | [@ganeshark04](https://github.com/ganeshark04) |
| **Nuthan Kumar K** | Backend & AI Integration | TBD |
| **Prabhakara R** | Frontend & UI/UX Design | TBD |

---

## 🎨 UI/UX Highlights

- **Dark Theme** with purple (#7c3aed) and blue (#3b82f6) gradient accents
- **Particle Animation** background for visual appeal and sophistication
- **Real-time Updates** for instant feedback and responsiveness
- **Mobile Responsive** design for all screen sizes
- **Accessibility** considerations throughout (proper contrast, semantic HTML)
- **Professional Branding** with DataNexus logo and consistent design
- **Smooth Animations** with CSS transitions and Canvas effects

---

## 🔧 Configuration

### Environment Variables
```env
GROQ_API_KEY=your_groq_api_key_here
```

### OpenMetadata Defaults (from docker-compose.yml)
```
URL: http://localhost:8585
Email: admin@open-metadata.org
Password: admin
Port: 8585
```

### Backend Server
```
Host: 0.0.0.0
Port: 8000
Framework: FastAPI
```

---

## 📊 Sample Interactions

### Chat with AI
```
User: "What tables contain customer data?"

AI Response: "Based on the OpenMetadata catalog, the following tables 
contain customer data:

- raw_customer: Raw customer table with personal information
- dim_customer: Dimension table with aggregated customer details
- dim_address: Address information with PII

These tables contain sensitive information and require special care 
and proper access controls."
```

### Explore Lineage
```
User: "Show lineage of dim_customer"

App Response: [Visual flow diagram]

raw_customer (Source Database)
    ↓
staging_customer (dbt transformation)
    ↓
dim_customer (Data Warehouse)
    ↓
sales_dashboard (BI Report)

Additional Info: 3 downstream dependencies, 1 upstream source
```

### Check Data Quality
```
User: "Show data quality issues"

App Response: [Quality Metrics Screen]

- column_value_max_to_be_between: shop_id (UNKNOWN)
- column_values_to_be_between: zip (UNKNOWN)
- column_values_to_match_regex: last_name (UNKNOWN)
- diff_columns: dim_address (UNKNOWN)
- diff_with_production: dim_address (UNKNOWN)

Data Governance Status: All Systems Operational
```

---

## 🏆 Key Achievements

✅ **Real OpenMetadata Integration** — Live connection to actual data catalog  
✅ **AI-Powered Chat** — Groq AI with context-aware intelligent responses  
✅ **Beautiful UI** — Professional dark theme with particle effects  
✅ **Real-Time APIs** — Actual lineage, quality, and PII data (not mocked)  
✅ **Production-Ready** — Async handling, error management, caching, optimization  
✅ **Zero Dependencies** — Frontend requires no frameworks (vanilla JS)  
✅ **Fast Performance** — Token caching, connection pooling, optimized queries  
✅ **Well Documented** — Complete README, installation guide, inline comments  
✅ **Docker Ready** — One command setup with docker-compose  

---

## 🚀 Future Enhancements

- [ ] Advanced natural language processing for complex semantic queries
- [ ] Impact analysis - understand what breaks if you delete a table
- [ ] Data governance workflows and approval processes
- [ ] Anomaly detection with ML models
- [ ] Team collaboration features and shared workspaces
- [ ] Mobile app version (React Native)
- [ ] Multi-language support (i18n)
- [ ] Custom data classification rules
- [ ] Automated remediation workflows
- [ ] Slack/Teams integration for notifications
- [ ] Export capabilities (reports, lineage diagrams)
- [ ] Advanced search with filters and facets

---

## 📁 Project Structure

```
datanexus-ai-chat/
├── backend.py                 # FastAPI backend with all endpoints
├── index.html                 # Frontend UI with vanilla JS
├── docker-compose.yml         # OpenMetadata Docker setup
├── favicon.png               # DataNexus logo
├── requirements.txt          # Python dependencies
├── .env                      # Environment variables (not in git)
├── .gitignore               # Git ignore rules
├── README.md                # This file
└── INSTALLATION.md          # Detailed installation guide
```

---

## 🔐 Security & Best Practices

- ✅ API keys stored in `.env` (never committed to git)
- ✅ CORS enabled for frontend-backend communication
- ✅ Token caching with TTL (3500 seconds)
- ✅ Async request handling prevents blocking
- ✅ Connection pooling for database efficiency
- ✅ Error handling on all API endpoints
- ✅ Input validation on chat messages
- ✅ Keyword extraction to prevent injection

---

## 📝 License

MIT License - See LICENSE file for details

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📞 Support

For issues, questions, or suggestions:
- Open an issue on [GitHub](https://github.com/ganeshark04/datanexus-ai-chat/issues)
- Check [OpenMetadata docs](https://docs.open-metadata.org)
- Check [Groq API docs](https://console.groq.com/docs)
- Review [INSTALLATION.md](INSTALLATION.md) for setup help

---

## 🙏 Acknowledgments

- **OpenMetadata** — For the amazing data catalog platform
- **Groq** — For the blazing-fast AI inference with LLaMA
- **WeMakeDevs** — For organizing this incredible hackathon
- **FastAPI** — For the modern Python web framework
- **Claude AI** — For development assistance and guidance
- Our team for the incredible effort, innovation, and dedication

---

## 📸 Demo Video

https://youtu.be/QzkgCAnJK3A

Check out the demo video to see DataNexus AI Chat in action!

---

## 🎓 Learning & Inspiration

This project was built to demonstrate:
- Integration of multiple APIs (OpenMetadata, Groq)
- Modern async Python with FastAPI
- Responsive frontend without heavy frameworks
- Docker containerization
- AI-powered feature development
- Rapid prototyping during hackathons

---

## 📊 Statistics

- **Lines of Code:** 1000+
- **API Endpoints:** 10+
- **Frontend Components:** 50+
- **Development Time:** 9 days
- **Team Size:** 3 developers
- **Technologies Used:** 15+
- **Docker Containers:** 5

---

**Built with ❤️ during the WeMakeDevs × OpenMetadata Hackathon**

**April 2026 - "Back to the Metadata" Challenge**

**GitHub:** https://github.com/ganeshark04/datanexus-ai-chat

**Team:** Gagan Rao K, Nuthan Kumar K, Prabhakara R

---

## 🎬 How to Get Started

1. Clone the repo: `git clone https://github.com/ganeshark04/datanexus-ai-chat`
2. Follow [INSTALLATION.md](INSTALLATION.md) for setup
3. Get Groq API key from https://console.groq.com
4. Run `python backend.py`
5. Open browser and start asking questions!

**Questions?** Check the [INSTALLATION.md](INSTALLATION.md) guide or open an issue.

---

**Let's connect data with intelligence!** 🚀
