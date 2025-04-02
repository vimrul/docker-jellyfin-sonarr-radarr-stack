# 🧰 Docker Jellyfin Sonarr Radarr Stack

A powerful and fully self-hosted **media server stack** built using **Docker Compose**, featuring **Jellyfin**, **Sonarr**, **Radarr**, **Bazarr**, **qBittorrent**, **Prowlarr**, **Readarr**, **Jellyseerr**, **Firefox browser**, **Duplicati** backups, and **FlareSolverr** for indexer unlocking.

Ideal for self-hosters, media hoarders, and home lab enthusiasts who want to automate and manage their entire media ecosystem.

---

## 📦 Services Included

| Service       | Description                                 | Port  |
|--------------|---------------------------------------------|--------|
| **Jellyfin**   | Media server for streaming movies & TV      | 8096   |
| **Sonarr**     | TV show downloader/manager                  | 8989   |
| **Radarr**     | Movie downloader/manager                    | 7878   |
| **Readarr**    | eBook/audioBook downloader/manager          | 8787   |
| **Bazarr**     | Subtitle downloader                         | 6767   |
| **Prowlarr**   | Indexer manager for Sonarr/Radarr/etc       | 9696   |
| **qBittorrent**| Torrent client with Web UI                  | 8080   |
| **Jellyseerr** | Request management for Jellyfin             | 5055   |
| **Duplicati**  | Backup service                              | 8200   |
| **Firefox**    | Browser in container (VNC/Web-based)        | 3001   |
| **FlareSolverr**| CAPTCHA solving proxy for Prowlarr         | 8191   |

---

## 🚀 Features

- 🐳 Easy to deploy with Docker Compose
- 🖁️ Fully automated download and media management
- 🎮 Stream your content from Jellyfin across devices
- 📂 Download, organize, subtitle, and request media effortlessly
- 🔒 Backup configs and settings with Duplicati
- 🔧 Built-in health checks for monitoring uptime
- 🌍 Accessible from your local network or securely over the internet

---

## 📁 Folder Structure

```
🔹 configs/
├── jellyfin/
├── firefox/
├── duplicati/
└── mediarr/
    ├── radarr/
    ├── sonarr/
    ├── bazarr/
    ├── prowlarr/
    ├── jellyseerr/
    └── qbittorrent/
🔹 docker-compose.yml
```

---

## 🛠️ Requirements

- Docker Engine & Docker Compose
- Access to `/dev/dri/renderD128` for hardware acceleration (optional)
- External HDD/SSD or mounted folders for:
  - `/mnt/media`
  - `/mnt/HDD/downloads`

---

## 🔧 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/docker-jellyfin-sonarr-radarr-stack.git
cd docker-jellyfin-sonarr-radarr-stack
```

### 2. Configure Volumes
Update the paths in `docker-compose.yml` to match your system directories.

### 3. Launch the Stack
```bash
docker compose up -d
```

