<div align="center">
  <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="120">

  <h1>Robert Carvalho</h1>

  <a href="https://github.com/robcarv">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1000&color=1DB954&center=true&vCenter=true&width=600&lines=QA+Automation+Engineer+%40+IBM;Homelab+%7C+Infrastructure+%7C+Automation;Python+%7C+Playwright+%7C+Docker;3+Raspberry+Pis+%2B+TrueNAS+Scale+10.9TB;55%2B+Services+Monitored+24%2F7;AI+Agent+Automation+%7C+Cron+Pipelines" alt="Typing SVG">
  </a>

  <br>
  <br>

  <a href="https://robcarv.github.io">
    <img src="https://img.shields.io/badge/Portfolio-robcarv.github.io-1DB954?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio">
  </a>
  <a href="https://linkedin.com/in/rac-carvalho">
    <img src="https://img.shields.io/badge/LinkedIn-rac--carvalho-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="https://instagram.com/chch_changes">
    <img src="https://img.shields.io/badge/Instagram-chch__changes-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram">
  </a>
  <a href="https://github.com/robcarv">
    <img src="https://img.shields.io/badge/GitHub-robcarv-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
</div>

---

## 🏠 Homelab Infrastructure

**3 Raspberry Pis + TrueNAS Scale** — 55+ Docker containers monitored 24/7

| Device | Specs | Services |
|--------|-------|----------|
| 🟢 **Pi 501** | 4-core · 8GB | Hermes Agent, Gallery Downloader, Dashy, Nginx Proxy Manager, Wallos, Uptime Kuma, Speedtest Tracker, Changedetection, Prowlarr, Glances, Portainer Agent |
| 🟢 **Pi 5** | 4-core · 8GB | AzuraCast (Dublin Calling), DuckDNS, qBittorrent, IPRoyal, Glances |
| 🟢 **Pi 4** | 4-core · 4GB | Dashy, Duplicati, CVE Scanner (Trivy), Portainer, Glances |
| 🟣 **TrueNAS** | Scale · 10.9TB NVMe | Jellyfin, Immich, Tailscale, SMB Shares |

**Dashboards & Monitoring:**

| Dashboard | Access |
|-----------|--------|
| [Portfolio](https://robcarv.github.io) | Live health: CPU, RAM, temp, containers, radio |
| [Uptime Kuma](https://uptimehome.duckdns.org/dashboard) | 55+ service uptime monitoring |
| Dashy | `Pi501:8200` / `Pi4:8200` (local network) |
| Hermes Dashboard | `Pi501:9119` (local network) |

---

## 📻 Dublin Calling Radio

> Irish independent radio station — 24/7 streaming from Pi 5

<p align="center">
  <a href="https://dublincalling.duckdns.org/public/dublincalling">
    <img src="https://img.shields.io/badge/Listen_Live-Dublin_Calling-1DB954?style=for-the-badge&logo=musicbrainz&logoColor=white" alt="Listen Live">
  </a>
  &nbsp;
  <a href="https://t.me/Siteschanges_bot">
    <img src="https://img.shields.io/badge/Request_Song-@Siteschanges__bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Request Song">
  </a>
</p>

**Source code:** [azura-cast-customizations](https://github.com/robcarv/azura-cast-customizations) — Glassmorphism theme for the public page

---

## 🚀 Active Projects

| Project | Stack | Description |
|---------|-------|-------------|
| [robcarv.github.io](https://github.com/robcarv/robcarv.github.io) ![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat&logo=html5&logoColor=white) | HTML · CSS · JS | Portfolio site with live homelab health, radio player, news feed |
| [news_colletector](https://github.com/robcarv/news_colletector) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) | Python · RSS · TTS | RSS collector — 17 feeds, Edge-TTS PT/EN audio, Telegram delivery |
| [dashy-homelab](https://github.com/robcarv/dashy-homelab) ![YAML](https://img.shields.io/badge/YAML-CB171E?style=flat&logo=yaml&logoColor=white) | YAML · Docker | Dashy dashboard config — 55+ services, Glances widgets, dark theme |
| [azura-cast-customizations](https://github.com/robcarv/azura-cast-customizations) ![JS](https://img.shields.io/badge/JS-F7DF1E?style=flat&logo=javascript&logoColor=black) | CSS · JS | AzuraCast public page theme — glassmorphism, custom player, dark mode |
| [gallery-downloader](https://github.com/robcarv) *(private)* | Go · React · Redis | Media downloader — Go/Gin backend, React frontend, PostgreSQL+Redis queue |

---

## ⚡ Automations & Cron Jobs

> Automated pipelines running via Hermes Agent, keeping everything in sync

| Pipeline | Schedule | What it does |
|----------|----------|--------------|
| 🩺 **Health Monitor** | Every 60min | Collects CPU, RAM, temp, load, disk, containers from 3 Pis via Glances API |
| 📊 **Portfolio Push** | Every 60min | Generates `health.json` + syncs `news.json`, pushes to GitHub Pages |
| 📰 **News Sync** | Every 30min | Copies latest RSS news from NewsBot to portfolio |
| 💾 **Backup Pipeline** | Daily | Backs up configs and data across all 3 Pis |
| 🔒 **CVE Scanner** | Every 6h | Trivy vulnerability scan on containers (Pi 4) |

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|-------------|
| **Languages** | Python, Java, JavaScript, SQL, Bash |
| **Testing** | Playwright, Selenium, JUnit, Rest Assured, Locust, K6 |
| **CI/CD** | Jenkins, GitHub Actions, Git |
| **Infrastructure** | Docker, Docker Compose, Raspberry Pi, TrueNAS Scale, Nginx |
| **Monitoring** | Glances, Uptime Kuma, Speedtest Tracker, Changedetection |
| **AI & Automation** | Hermes Agent (CLI AI), Cron Jobs, RSS Pipelines |
| **Media** | AzuraCast, Jellyfin, qBittorrent |

---

## 📚 Learning & Legacy

| Repository | Description |
|-----------|-------------|
| [Ansible-3-layers](https://github.com/robcarv/Ansible-3-layers) | Ansible automation — 3-layer architecture |
| [jenkins-todo-list](https://github.com/robcarv/jenkins-todo-list) | Django todo list with Jenkins CI/CD pipeline |
| [Data_science_alura](https://github.com/robcarv/Data_science_alura) | Data Science coursework (Alura) |
| [basicstuff](https://github.com/robcarv/basicstuff) | Basic programming exercises |
| [beginner-project](https://github.com/robcarv/beginner-project) | Beginner Python projects |
| [2021](https://github.com/robcarv/2021) | Early projects archive |

---

<div align="center">

  <img src="https://komarev.com/ghpvc/?username=robcarv&color=1DB954&style=flat-square" alt="Profile views">

  <br>
  <br>

  <a href="https://github.com/robcarv">
    <img src="https://github-readme-stats.vercel.app/api?username=robcarv&show_icons=true&theme=dracula&hide_border=true&count_private=true&hide_title=true" alt="GitHub Stats" width="48%">
  </a>
  <a href="https://github.com/robcarv">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=robcarv&layout=compact&theme=dracula&hide_border=true&hide_title=true" alt="Top Languages" width="42%">
  </a>

  <br>
  <br>

  <sub>Built with ☘️ in Dublin, running on Raspberry Pi</sub>

</div>
