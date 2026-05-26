# 🌫️ PM2.5 Monitor

A real-time PM2.5 air quality monitoring application using GPS and Claude AI.

## 🔗 Links
- **Live App**: cerulean-entremet-8fc9c2.netlify.app
- **Demo Video**: https://youtube.com/shorts/gQN6dp3YzEM?feature=share

## ✨ Features
- Real-time AQI monitoring via GPS
- Claude AI (via OpenRouter) analysis and personalized recommendations
- Email reports delivered through N8N Workflow
- 7-day historical AQI chart
- Alert system when AQI exceeds a configured threshold
- Auto-refresh every 30 minutes
- PWA support (installable on mobile)

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| Frontend | HTML / CSS / JavaScript |
| Hosting | Netlify |
| Air Quality Data | AQICN.org API |
| AI Analysis | Claude Haiku via OpenRouter |
| Backend Automation | N8N Workflow |

## 📁 File Structure

```
pm25-monitor/
├── index.html          # Main application
├── manifest.json       # PWA configuration
└── README.md           # This file
```

## 🚀 How to Deploy

### 1. Clone Repository
```bash
git clone https://github.com/[username]/pm25-monitor.git
cd pm25-monitor
```

### 2. Deploy to Netlify
1. Go to [netlify.com](https://netlify.com)
2. Click **Add new site** → **Deploy manually**
3. Drag and drop the entire project folder
4. Receive your URL automatically

### 3. Setup N8N Workflow
1. Import `PM2_5_GPS_Alert_v2.json` into N8N
2. Configure Gmail / SMTP credentials
3. Configure Google Sheets credentials
4. Activate the workflow
5. Update `WEBHOOK_URL` in index.html

## 📊 AQI Levels

| AQI | Status | Recommendation |
|-----|--------|----------------|
| 0–50 | Good 🟢 | All outdoor activities are fine |
| 51–100 | Moderate 🟡 | Sensitive groups should take precautions |
| 101–150 | Unhealthy for Sensitive Groups 🟠 | Reduce outdoor activities |
| 151–200 | Unhealthy 🔴 | Wear an N95 mask |
| 201+ | Very Unhealthy 🟣 | Avoid going outdoors |


## 📄 License
MIT License
