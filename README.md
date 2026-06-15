<div align="center">
  <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="120">
  
  <h1>🇮🇪 Robert Carvalho</h1>

  <a href="https://github.com/robcarv">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1000&color=1DB954&center=true&vCenter=true&width=600&lines=QA+Automation+Engineer;Homelab+%26+Infrastructure+Enthusiast;Python+%2B+Playwright+%2B+Java;55%2B+services+monitored+24%2F7;3+Raspberry+Pis+%2B+TrueNAS+Scale" alt="Typing SVG" />
  </a>

  <br><br>

  <a href="https://robcarv.github.io">
    <img src="https://img.shields.io/badge/-🌐_Portfolio-robcarv.github.io-915eff?style=for-the-badge" alt="Portfolio" />
  </a>
  <a href="https://robcarv.github.io/homelab-architecture/">
    <img src="https://img.shields.io/badge/-🏠_Architecture_Diagram-915eff?style=for-the-badge" alt="Architecture" />
  </a>
</div>

---

### ⚙️ **Tech Stack**

<div align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=py,java,docker,linux,raspberrypi,postgres,terraform,ansible,azure,kubernetes&theme=dark&perline=10" alt="Tech Stack" />
  </a>
</div>

---

### 🏡 **Homelab Architecture**

```
🌐 INFRASTRUCTURE
├── Pi4 (192.168.68.102) → Pi-hole, Dashy, NPM, Wallos, Glances
├── Pi5-108 (192.168.68.108) → AzuraCast, qBittorrent, ClamAV, DuckDNS, Glances
├── Pi501-117 (192.168.68.117) → Indexer Mgr, Download Mgr, UptimeKuma, ChangeDetection, Speedtest
└── TrueNAS Scale (192.168.68.124) → NVMe 10.9TB, Jellyfin, CIFS Shares, 88 media files

📦 ORCHESTRATION
├── Docker + Docker Compose (20+ containers across 3 Pis)
├── Portainer (visual container management)
└── Glances (real-time CPU/RAM/disk/temp on all Pis)

🖥️ CORE SERVICES
├── Dashy           → Central dashboard (30+ services)
├── Portfolio       → robcarv.github.io (3D + health + radio + news)
├── UptimeKuma      → 55+ services monitored (48 UP)
├── Pi-hole         → DNS ad blocker
├── Nginx Proxy Manager → SSL reverse proxy
├── AzuraCast       → Dublin Calling web radio (2GB RAM limit)
├── Wallos          → Subscription management
├── Speedtest Tracker → Network speed monitoring
├── ChangeDetection → Website change monitor
└── Gallery Downloader v2 → Multi-source download manager with queue

🎬 MEDIA PIPELINE
├── Indexer Manager
├── Download Manager
├── ClamAV          → Daily antivirus scan (3GB RAM, 0 threats)
└── Jellyfin        → Media streaming on TrueNAS

🔒 BACKUP & SECURITY
├── ClamAV (daily scan at 03:00, 0 threats found)
├── Rsync to TrueNAS (daily at 04:00)
├── Full backup + health report (Mon/Wed/Fri 03:30)
├── Health guardian (checks load/RAM/swap every 5min)
├── CIFS auto-mounter (reconnects every 5min)
├── Automated Git push to GitHub (3 repos)
└── DuckDNS (dynamic DNS for radio and portfolio)

📊 MONITORING
├── UptimeKuma (55+ services, 48 UP, instant alerts)
├── Glances on all 3 Pis (CPU, RAM, disk, temperature)
├── Pi Health Report (auto score 0-100 for each Pi)
├── Torrent health check (every 6h, rechecks stuck items)
├── Media health check (every 2h)
└── Guardian (prevents OOM by pausing downloads)

🤖 AUTOMATION
├── NewsBot (cron 08:00, 20:00)
│   ├── Collects RSS from 17 feeds
│   ├── LLM summarization + TTS audio
│   ├── Sends to Telegram
│   └── Auto-pushes to GitHub → portfolio updates
├── Health Report (integrated with backup)
│   ├── Collects metrics from all 3 Pis
│   ├── Generates health.json → portfolio
│   └── Auto-pushes to GitHub
└── Backup Pipeline
    ├── ClamAV antivirus scan
    ├── Rsync to TrueNAS
    ├── Health report generation
    └── Git push to GitHub
```

---

### 🖼️ **Gallery Downloader v2** — Featured Project

Multi-source download manager with sequential queue, smart cache, and automatic fallback recovery.

| Feature | Stack |
|---|---|
| **Queue** | In-memory + SQLite persistence, strict FIFO, auto-retry |
| **Sources** | 3 sources, pluggable via ScraperBase |
| **Fallback** | 5 strategies (scraper, cloudscraper, curl_cffi, requests, direct) |
| **Cache** | SQLite TTL cache, incremental merge |
| **Web UI** | Flask dashboard with real-time SSE events |
| **Monitoring** | Watchdog auto-restarts workers if stuck |

```mermaid
graph TB
    CLI["CLI Menu"] --> Q["DownloadQueue\n(1 per vez)"]
    WEB["Web UI :8788"] --> Q
    Q --> S["Scraper Manager"]
    S --> N1["Source 1"] & N2["Source 2"] & N3["Source 3"]
    Q --> DB[(SQLite Cache)]
    S --> TN["TrueNAS 6TB"]
```

**Branch v2** — github.com/robcarv/backup_raspberry

---

### 📊 **System Health**

<div align="center">

| Pi | Status | Score | Uptime | Temp | RAM | Disk | Containers |
|---|---|---|---|---|---|---|---|
| **Pi4** | 🟢 Excellent | 100/100 | Up | ~30°C | ~9% | ~16% | 7 |
| **Pi5-108** | 🟢 Good | 90/100 | Up | ~48°C | ~25% | ~64% | 8 |
| **Pi501-117** | 🟢 Good | 75/100 | Up | ~48°C | ~25% | ~35% | ~12 |

</div>

> 📈 **Live health dashboard**: https://robcarv.github.io (System Health section)
> 🔄 Auto-updated every backup (Mon/Wed/Fri) and NewsBot run (08:00, 20:00)

---

### 🕐 **Cron Schedule**

| Time | Task | Location |
|---|---|---|
| Every 5min | Guardian (load/RAM/swap check) | Pi5-108 |
| Every 5min | CIFS auto-mount check | Pi5-108 |
| Every 6h | Health recheck | Pi5-108 |
| 03:00 daily | ClamAV antivirus scan | Pi5-108 |
| 03:30 Mon/Wed/Fri | Full backup + health report | Pi5-108 |
| 04:00 daily | Rsync to TrueNAS | Pi5-108 |
| 08:00 / 20:00 | NewsBot RSS → Telegram → Push GitHub | Pi 501 |
| Every 2h | Media health check | Pi 501 |

---

### 📊 **GitHub Analytics**

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=robcarv&theme=tokyonight&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&show=reviews,discussions_answered,prs_merged" alt="GitHub Stats" height="180"/>
  <img src="https://streak-stats.demolab.com?user=robcarv&theme=tokyonight&hide_border=true" alt="GitHub Streak" height="180"/>
</div>

<br>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=robcarv&theme=tokyonight&hide_border=true&layout=compact&langs_count=8&hide=html,css,scss" alt="Top Languages" height="160"/>
</div>

---

### 🚀 **Featured Projects**

<div align="center">

[![Portfolio](https://github-readme-stats.vercel.app/api/pin/?username=robcarv&repo=robcarv.github.io&theme=tokyonight&hide_border=true)](https://robcarv.github.io)
[![News Collector](https://github-readme-stats.vercel.app/api/pin/?username=robcarv&repo=news_colletector&theme=tokyonight&hide_border=true)](https://github.com/robcarv/news_colletector)
[![Backup Raspberry](https://github-readme-stats.vercel.app/api/pin/?username=robcarv&repo=backup_raspberry&theme=tokyonight&hide_border=true)](https://github.com/robcarv/backup_raspberry)
[![Dashy Homelab](https://github-readme-stats.vercel.app/api/pin/?username=robcarv&repo=dashy-homelab&theme=tokyonight&hide_border=true)](https://github.com/robcarv/dashy-homelab)

</div>

---

### 📻 **Listen Live — Dublin Calling**

<div align="center">
  <a href="https://dublincalling.duckdns.org/public/dublincalling" target="_blank">
    <img src="https://img.shields.io/badge/-Listen_Live-Dublin_Calling-1DB954?style=for-the-badge&logo=materialdesignicons&logoColor=white" alt="Listen Live"/>
  </a>
  <br><br>
  <img src="https://dublincalling.duckdns.org/api/nowplaying/dublincalling/art" width="200" style="border-radius: 12px;" alt="Now Playing"/>
</div>

---

### 📡 **Connect**

<div align="center">
  <a href="https://robcarv.github.io"><img src="https://img.shields.io/badge/-Portfolio-000?style=for-the-badge&logo=react&color=915eff" alt="Portfolio" /></a>
  <a href="https://linkedin.com/in/rac-carvalho"><img src="https://img.shields.io/badge/-LinkedIn-000?style=for-the-badge&logo=linkedin&color=0A66C2" alt="LinkedIn" /></a>
  <a href="https://github.com/robcarv"><img src="https://img.shields.io/badge/-GitHub-000?style=for-the-badge&logo=github&color=181717" alt="GitHub" /></a>
  <a href="mailto:robert_carvalho@hotmail.com"><img src="https://img.shields.io/badge/-Email-000?style=for-the-badge&logo=microsoft-outlook&color=0078D4" alt="Email" /></a>
  <a href="https://dublincalling.duckdns.org/public/dublincalling"><img src="https://img.shields.io/badge/-Dublin_Calling_Radio-000?style=for-the-badge&logo=radio&color=1DB954" alt="Radio" /></a>
</div>

---

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/robcarv/robcarv/output/github-contribution-grid-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/robcarv/robcarv/output/github-contribution-grid-snake.svg">
    <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/robcarv/robcarv/output/github-contribution-grid-snake.svg">
  </picture>
  <br>
</div>
