<div align="center">
  <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="120">

  <h1>Robert Carvalho</h1>

  <a href="https://github.com/robcarv">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1000&color=1DB954&center=true&vCenter=true&width=600&lines=QA+Automation+Engineer;Homelab+%26+Infrastructure+Enthusiast;Python+%2B+Playwright+%2B+Java;55%2B+services+monitored+24%2F7;3+Raspberry+Pis+%2B+TrueNAS+Scale" alt="Typing SVG">
  </a>

  <br>

  <a href="https://robcarv.github.io">
    <img src="https://img.shields.io/badge/Portfolio-robcarv.github.io-1DB954?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio">
  </a>
  <a href="https://linkedin.com/in/rac-carvalho">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="https://github.com/robcarv">
    <img src="https://img.shields.io/badge/GitHub-robcarv-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
</div>

---

## Infrastructure

Homelab with 3 Raspberry Pis + TrueNAS Scale (NVMe 10.9TB):

| Device | IP | Role |
|--------|----|------|
| Pi 4 | 192.168.68.102 | Pi-hole, Nginx Proxy Manager, Wallos, Duplicati |
| Pi 5 | 192.168.68.108 | AzuraCast (Dublin Calling radio), Uptime Kuma |
| Pi 501 | 192.168.68.117 | Hermes Agent, Dashy, Speedtest Tracker, Discount Bandit |
| TrueNAS | 192.168.68.124 | NVMe pool 10.9TB, Jellyfin, Immich, Tailscale |

**Dashboards:**
- Dashy: http://192.168.68.117:8200 | http://192.168.68.102:8200
- Hermes Dashboard: http://192.168.68.117:9119
- Uptime Kuma: https://uptimehome.duckdns.org/dashboard

**Radio:**
- [Dublin Calling](https://dublincalling.duckdns.org/public/dublincalling) - Irish independent radio station
- Request a song: https://t.me/Siteschanges_bot

---

## Repositories

### Active Projects

| Repository | Description | Branch |
|-----------|-------------|--------|
| [news_colletector](https://github.com/robcarv/news_colletector) | RSS feed collector with TTS and Telegram delivery. 17 feeds, Edge-TTS PT/EN. | `main`, `legacy-v1` |
| [azura-cast-customizations](https://github.com/robcarv/azura-cast-customizations) | Visual customizations for AzuraCast public page. Glassmorphism theme for Dublin Calling radio. | `main` |
| [dashy-homelab](https://github.com/robcarv/dashy-homelab) | Dashy dashboard config for homelab cluster (Pi4, Pi5, Pi501). 55+ services, Glances monitoring. | `main` |
| [robcarv.github.io](https://github.com/robcarv/robcarv.github.io) | Portfolio site - QA Automation Engineer. | `main` |

### Learning & Legacy

| Repository | Description | Branch |
|-----------|-------------|--------|
| [Ansible-3-layers](https://github.com/robcarv/Ansible-3-layers) | Ansible automation - 3 layer architecture | `main` |
| [Data_science_alura](https://github.com/robcarv/Data_science_alura) | Data science coursework (Alura) | `master` |
| [jenkins-todo-list](https://github.com/robcarv/jenkins-todo-list) | Django todo list with Jenkins CI/CD pipeline | `master` |
| [basicstuff](https://github.com/robcarv/basicstuff) | Basic programming exercises | `main` |
| [beginner-project](https://github.com/robcarv/beginner-project) | Beginner projects | `main` |
| [2021](https://github.com/robcarv/2021) | Early projects from 2021 | `master` |

### Dashy (mirror)

| Repository | Description |
|-----------|-------------|
| [Dashy](https://github.com/robcarv/Dashy) | Dashy dashboard config file (personal mirror) |

---

## Services

### Radio & Entertainment
- **Dublin Calling** - Irish independent radio station (AzuraCast on Pi5)
- **Listen live**: https://dublincalling.duckdns.org/public/dublincalling
- **Jellyfin** - Media server (TrueNAS)

### Infrastructure
- **Pi-hole** - DNS ad-blocker (Pi4)
- **Uptime Kuma** - Service monitoring (Pi5)
- **Glances** - System monitoring on all Pis (port 61208)
- **Speedtest Tracker** - Network speed monitoring (Pi501)
- **Changedetection** - Website change monitoring (Pi5)

### Development & DevOps
- **Hermes Agent** - AI CLI agent (Pi501, dashboard on port 9119)
- **Portainer** - Docker management (Pi4)
- **Nginx Proxy Manager** - Reverse proxy (Pi501)
- **NewsBot** - RSS news collector with TTS audio (GitHub)

### Storage & Backup
- **TrueNAS Scale** - NVMe pool 10.9TB, SMB shares
- **Duplicati** - Automated backups (Pi4 + Pi5)
- **Tailscale** - VPN mesh (all devices)

---

## Tech Stack

**Languages:** Python, Java, JavaScript, SQL, Bash
**Testing:** Playwright, Selenium, JUnit, Rest Assured, Locust, K6
**CI/CD:** Jenkins, GitHub Actions
**Infrastructure:** Docker, Raspberry Pi, TrueNAS Scale, Nginx, Pi-hole
**Monitoring:** Glances, Uptime Kuma, Speedtest Tracker
**Tools:** Hermes Agent (AI CLI), Dashy (dashboard), AzuraCast (radio)

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=robcarv&color=1DB954&style=flat-square" alt="Profile views">
  <br>
  <img src="https://github-readme-stats.vercel.app/api?username=robcarv&show_icons=true&theme=dracula&hide_border=true&count_private=true" alt="GitHub Stats" width="48%">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=robcarv&layout=compact&theme=dracula&hide_border=true" alt="Top Languages" width="42%">
</div>
