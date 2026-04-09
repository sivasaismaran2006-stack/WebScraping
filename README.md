# Email Scraper & Validator with Gemini API

A full-stack web application for scraping, validating, and analyzing emails using Google's Gemini AI API.

## 🎯 Features

- 🔍 **Web Email Scraping** - Extract emails from URLs
- ✅ **Email Validation** - Syntax, domain, and SMTP verification
- 🤖 **Gemini AI Analysis** - Analyze emails for spam, authenticity, etc.
- 📊 **Dashboard** - Clean, intuitive user interface
- 📈 **History & Analytics** - Track all scraping and validation activities
- 📥 **Export** - Download results as CSV or JSON
- 🔐 **Secure** - Environment-based configuration

## 🛠 Tech Stack

- **Backend**: Python 3.9+, Flask, Flask-CORS
- **Frontend**: React 18+, Axios, React Router
- **Database**: SQLite
- **API**: Google Gemini API
- **Containerization**: Docker & Docker Compose

## 📁 Project Structure

```
WebScraping/
├── backend/
│   ├── app.py                 # Main Flask application
│   ├── config.py              # Configuration management
│   ├── requirements.txt        # Python dependencies
│   ├── .env.example           # Environment variables template
│   ├── routes/
│   │   ├── scraper.py         # Email scraping endpoints
│   │   ├── validator.py       # Email validation endpoints
│   │   └── gemini.py          # Gemini AI endpoints
│   ├── services/
│   │   ├── scraper_service.py # Web scraping engine
│   │   ├── validator_service.py # Email validation logic
│   │   └── gemini_service.py  # Gemini API integration
│   └── utils/
│       └── logger.py          # Logging configuration
├── frontend/
│   ├── package.json           # Node.js dependencies
│   ├── public/
│   │   └── index.html
│   └── src/
│       ├── App.jsx            # Main React component
│       ├── index.js           # React entry point
│       └── styles/
│           └── App.css
├── docker-compose.yml         # Docker compose configuration
└── README.md
```

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- Node.js 14+
- Google Cloud Console API Key (Gemini API)

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/sivasaismaran2006-stack/WebScraping.git
cd WebScraping
```

#### 2. Backend Setup

```bash
cd backend
cp .env.example .env
# Edit .env and add GEMINI_API_KEY
pip install -r requirements.txt
python app.py
```

Backend runs on http://localhost:5000

#### 3. Frontend Setup

```bash
cd frontend
npm install
npm start
```

Frontend runs on http://localhost:3000

## 🐳 Docker Setup

```bash
docker-compose up --build
```

## 📡 API Endpoints

- **POST /api/scrape** - Scrape emails from URL
- **POST /api/validate** - Validate email addresses
- **POST /api/gemini-analyze** - Analyze emails with Gemini AI
- **GET /api/history** - Get scraping history
- **GET /api/health** - Health check

## ⚙️ Environment Variables

```env
GEMINI_API_KEY=your_gemini_api_key_here
FLASK_ENV=production
DATABASE_URL=sqlite:///emails.db
CORS_ORIGINS=http://localhost:3000
```

## 🔐 Security

- API keys stored in environment variables
- CORS configuration for specified origins
- SMTP timeout to prevent hanging
- Input validation on all endpoints

## 🤝 Contributing

Contributions welcome! Fork, create feature branch, commit, push, and open PR.

## 📄 License

MIT License

---

Created with ❤️ for email management