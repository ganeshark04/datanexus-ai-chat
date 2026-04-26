# 🚀 Installation Guide

## Prerequisites

### Required
- **Docker Desktop** (https://www.docker.com/products/docker-desktop)
- **Python 3.10+** (https://www.python.org/downloads/)
- **Git** (https://git-scm.com/downloads)
- **Groq API Key** (free at https://console.groq.com)

### Verify Installation
```bash
# Check Python version
python --version  # Should be 3.10 or higher

# Check Docker
docker --version
docker compose --version

# Check Git
git --version
```

---

## Step-by-Step Installation

### 1. Clone Repository
```bash
git clone https://github.com/ganeshark04/datanexus-ai-chat
cd datanexus-ai-chat
```

### 2. Get Groq API Key
1. Go to https://console.groq.com
2. Sign up / Login
3. Create API key
4. Copy the key

### 3. Create `.env` File
```bash
# Windows (PowerShell)
echo "GROQ_API_KEY=gsk_YOUR_KEY_HERE" > .env

# Linux/Mac
echo "GROQ_API_KEY=gsk_YOUR_KEY_HERE" > .env
```

**Replace `gsk_YOUR_KEY_HERE` with your actual key!**

### 4. Start OpenMetadata Containers
```bash
docker compose up --detach
```

**Wait 2-3 minutes** for all containers to be ready. Check:
```bash
docker compose ps
```

All should show `Running` or `Healthy`

### 5. Install Python Dependencies
```bash
pip install -r requirements.txt
```

### 6. Run Backend Server
```bash
python backend.py
```

You should see:
```
✅ Token refreshed!
🚀 MetaChat ready!
🌐 Opened index.html in browser!
```

Browser opens automatically at `file:///path/to/index.html`

---

## 🔍 Troubleshooting

### Issue: "Docker not found"
**Solution:** Install Docker Desktop from https://docker.com

### Issue: "Python not found"
**Solution:** Install Python 3.10+ and add to PATH

### Issue: "Port 8585 already in use"
**Solution:**
```bash
# Stop existing Docker containers
docker compose down

# Then start again
docker compose up --detach
```

### Issue: "GROQ_API_KEY error"
**Solution:** Check `.env` file exists and has correct key format
```bash
# View .env content
cat .env  # Linux/Mac
type .env  # Windows PowerShell
```

### Issue: "OpenMetadata taking too long"
**Solution:** Wait 3-5 minutes for services to start fully
```bash
# Monitor logs
docker compose logs -f openmetadata_server
```

### Issue: "Browser doesn't open"
**Solution:** Manually open `index.html` in Chrome:
```bash
# Windows
start index.html

# Mac
open index.html

# Linux
xdg-open index.html
```

### Issue: "Chat not responding"
**Solution:** Ensure backend is running and check console for errors
```bash
# Kill backend
Ctrl+C

# Restart
python backend.py
```

---

## ✅ Verification

Once running, test each feature:

### 1. Test Backend Connection
```bash
curl http://localhost:8000/test
# Should return: {"status": "connected"}
```

### 2. Test Search
```bash
curl "http://localhost:8000/search?query=customer"
# Should return table results
```

### 3. Test Quality API
```bash
curl http://localhost:8000/quality
# Should return quality metrics
```

### 4. Test Chat
```bash
curl -X POST http://localhost:8000/chat \
  -H "Content-Type: application/json" \
  -d '{"message":"what tables exist"}'
# Should return AI response
```

---

## 🎯 First Steps

1. Open http://localhost in your browser
2. Type: "Show me customer tables"
3. Click "PII Scan" button
4. Click "Lineage" for a table
5. Click "Quality" to see alerts

---

## 📚 Next Steps

- Read the [README.md](README.md) for full documentation
- Check out [OpenMetadata docs](https://docs.open-metadata.org)
- Explore [Groq API docs](https://console.groq.com/docs)

---

## 🆘 Still Having Issues?

1. Check all error messages carefully
2. Ensure all ports are free (8000, 8585)
3. Verify `.env` file has correct API key
4. Try restarting Docker: `docker compose restart`
5. Check logs: `docker compose logs`

**Need help?** Open an issue on GitHub!
