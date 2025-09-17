# 🔄 Server Ping Workflow

This repository is dedicated to keeping my deployed apps awake by sending scheduled HTTP requests.  
It prevents "cold start" delays for users by ensuring the servers are periodically pinged.  

---

## 📌 How It Works
- Uses **GitHub Actions** to run on a schedule (via cron).  
- Sends an HTTP request (`curl`) to each app’s URL.  
- If the server is asleep, the ping wakes it up.  
- If the server is already awake, the ping just confirms it’s running.  
- If the server is down, it logs a warning in the workflow logs.  

---

## ⚙️ Setup Instructions

### 1. Clone this repo
```bash
git clone https://github.com/your-username/server-ping.git
cd server-ping
