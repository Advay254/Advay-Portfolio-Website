<div align="center">

<img src="https://img.shields.io/badge/Advay--Portfolio--Website-Latest-00e5ff?style=for-the-badge&logo=node.js&logoColor=white" alt="Advay Portfolio Website Latest" />

# 🚀 Advay Portfolio Website

### A full-featured developer portfolio and tools hub — self-hostable, CMS-driven, AI-powered.

[![Node.js](https://img.shields.io/badge/Node.js-18.x+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![Supabase](https://img.shields.io/badge/Supabase-Database-3ECF8E?style=flat-square&logo=supabase&logoColor=white)](https://supabase.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/Advay254/Advay-Portfolio-Website/pulls)
[![Deploy on Render](https://img.shields.io/badge/Deploy%20on-Render-46E3B7?style=flat-square&logo=render&logoColor=white)](https://render.com)

<br/>

<a href="https://www.buymeacoffee.com/advay254" target="_blank">
  <img src="https://img.shields.io/badge/Support%20Me-%E2%98%95%20Buy%20Me%20a%20Coffee-ffdd57?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black" alt="Buy Me A Coffee" />
</a>

<br/><br/>

> Your portfolio. Your brand. Your tools. All in one self-hostable app.

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=00E5FF&center=true&vCenter=true&width=600&lines=Portfolio+%7C+Tools+Hub+%7C+Personal+Brand;Full+CMS+Admin+Dashboard;AI+Chat+Assistant+Built+In;n8n+Webhook+Notifications;One-Time+Activation+%C2%B7+Deploy+Anywhere)](https://github.com/Advay254/Advay-Portfolio-Website)

</div>

---

## ✨ Features

<img align="right" width="380" src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="coding gif"/>

- 🏠 **Dynamic Homepage** — Animated hero, 3D rotating stack labels, smooth theme rotation, particle canvas
- 👤 **Profile & About** — Bio, avatar, skills, social links, specializations — all editable from admin
- 🗂️ **GitHub Repos** — Public repo showcase with collapsible README previews
- ⚡ **Live Tools** — Deployed tools grid with category filters
- ⚙️ **n8n Templates** — Downloadable automation workflow templates showcase
- 🤝 **Hire Me Form** — Contact form with service categories, quick info sidebar, intro text
- 🤖 **AI Chat Assistant** — In-page chat powered by Groq (scoped to portfolio context only)
- 💡 **Suggestion Box** — Floating visitor feedback widget
- 🔧 **Admin Dashboard** — Hidden CMS at a secret URL — manage everything without touching code
- 🔔 **n8n Webhook Notifications** — Instant alerts for new contact requests and suggestions
- 💳 **License System** — One-time activation per deployment
- 📊 **Page Views Tracking** — Built-in analytics visible from admin dashboard

<br clear="right"/>

---

## 🗂️ Project Structure

```
Advay-Portfolio-Website/
├── index.js          # Launcher — fetches and starts the core engine
├── package.json      # Launcher dependencies only
├── .env.example      # Environment variable reference
├── version.txt       # Current release version
└── .gitignore
```

> The core application is loaded securely at runtime. This keeps the source lean and the deployment simple.

---

## 🚀 Quick Start

### 1. Fork or clone the repo

```bash
git clone https://github.com/Advay254/Advay-Portfolio-Website.git
cd Advay-Portfolio-Website
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

```bash
cp .env.example .env
```

Edit `.env` with your values:

```env
DATABASE_URL=postgresql://postgres:[PASSWORD]@db.[PROJECT-REF].supabase.co:5432/postgres
ADMIN_PATH=your-secret-admin-path
ADMIN_USERNAME=admin
ADMIN_PASSWORD=your-secure-password
JWT_SECRET=your-long-random-secret
GROQ_API_KEY=gsk_xxxxxxxxxxxxxxxxxxxx
GROQ_MODEL=llama-3.3-70b-versatile
SITE_NAME=YourSiteName
```

### 4. Run

```bash
npm start
```

Visit `http://localhost:3000` — you're live. 🎉

---

## 🔑 Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `DATABASE_URL` | ✅ **Yes** | PostgreSQL / Supabase connection string. Get from: Supabase → Project Settings → Database → URI |
| `ADMIN_PATH` | ✅ **Yes** | Secret URL path for your admin dashboard. Example: `xk9m4a-panel` → admin at `/xk9m4a-panel` |
| `ADMIN_USERNAME` | ✅ **Yes** | Admin login username |
| `ADMIN_PASSWORD` | ✅ **Yes** | Admin login password — make it strong |
| `JWT_SECRET` | ✅ **Yes** | Long random string for session signing. Generate at [randomkeygen.com](https://randomkeygen.com) |
| `GROQ_API_KEY` | ✅ **Yes** | Powers the AI chat assistant. Get one free at [console.groq.com](https://console.groq.com) |
| `GROQ_MODEL` | Recommended | Groq model name. Default: `llama-3.3-70b-versatile` |
| `SITE_NAME` | Optional | Display name shown in the browser tab |
| `PORT` | Auto | Set automatically by Render — do not set manually |

---

## 🗄️ Database Setup (Supabase — Free Tier)

1. Create a free project at [supabase.com](https://supabase.com)
2. Go to **Project Settings → Database → Connection string → URI**
3. Copy the URI and set it as `DATABASE_URL` in your environment
4. Done — all database tables are created automatically on first run. No SQL needed.

---

## 🌐 Deploying to Production

### Render (recommended)

<img align="right" width="300" src="https://media.giphy.com/media/RbDKaczqWovIugyJmW/giphy.gif" alt="deploy gif"/>

1. Fork this repo to your GitHub account
2. Go to [render.com](https://render.com) and create a new **Web Service**
3. Connect your forked repo
4. Set **Build Command:** `npm install`
5. Set **Start Command:** `npm start`
6. Add your environment variables under **Environment**
7. Click **Deploy**

> Render free tier sleeps after 15 minutes of inactivity. Use [cron-job.org](https://cron-job.org) to ping `/health` every 10 minutes to keep it awake.

<br clear="right"/>

### Railway

```bash
npm install -g @railway/cli
railway login && railway init && railway up
```

Add your environment variables in the Railway dashboard under **Variables**.

### Any VPS (Ubuntu/Debian)

```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
git clone https://github.com/Advay254/Advay-Portfolio-Website.git
cd Advay-Portfolio-Website && npm install
npm install -g pm2
pm2 start index.js --name advay-portfolio
pm2 save && pm2 startup
```

---

## 🛠️ How It Works

```
User deploys Advay Portfolio Website
        ↓
Launcher starts and fetches the core engine securely at runtime
Core engine extracts and installs its own dependencies
        ↓
App starts — all pages and admin dashboard are ready
        ↓
Admin visits /{ADMIN_PATH} and logs in
Sets up profile, tools, repos, settings from the dashboard
        ↓
Visitors browse the portfolio, use the contact form, chat with the AI assistant
        ↓
New contact requests and suggestions fire instant webhook notifications
to your n8n instance — no need to log in to check manually
```

---

## 📊 Tech Stack

<div align="center">

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CDN-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-AI-F55036?style=for-the-badge)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)

</div>

---

## 🔄 Updates

Check `version.txt` for the latest release version. Sync your fork and redeploy on Render to get the latest update automatically.

---

## 🤝 Contributing

1. Fork the repo
2. Create your branch: `git checkout -b feature/your-feature`
3. Commit: `git commit -m 'Add your feature'`
4. Push: `git push origin feature/your-feature`
5. Open a Pull Request

---

## ⚠️ Disclaimer

This project is provided for personal use and self-hosting. The author is not responsible for misuse or downtime of third-party services.

---

## 📄 License

MIT © 2026 Advay — free to use, modify, and distribute.

---

<div align="center">

![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=Advay254.Advay-Portfolio-Website)

**If this saved you time, drop a ⭐ — it helps others find the project.**

<br/>

<a href="https://www.buymeacoffee.com/advay254" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;"></a>

</div>
