# 🏠 Homelab – Media & Services Stack

This repository contains my personal homelab setup built on Ubuntu Server using Docker and Nginx.

It provides a centralized landing page and multiple self-hosted services доступные через subdomains.

---

## 🚀 Features

* 📁 File management (Filebrowser)
* 🎬 Media streaming (Jellyfin)
* 🎵 Music server (Navidrome)
* ⬇️ Torrent client (qBittorrent)
* 🌐 Nginx reverse proxy with subdomains
* 🏠 Custom landing page (HTML dashboard)

---

## 🧩 Services

| Service     | Description          | Default Port |
| ----------- | -------------------- | ------------ |
| Filebrowser | File manager         | 8080         |
| Jellyfin    | Media server         | 8096         |
| Navidrome   | Music server         | 4533         |
| qBittorrent | Torrent client       | 8081         |

---

## 🌐 Access

Services are exposed via subdomains:

* `files.patsiomkinhomelab.com`
* `media.patsiomkinhomelab.com`
* `music.patsiomkinhomelab.com`
* `torrent.patsiomkinhomelab.com`

Landing page provides quick navigation to all services.

---

## ⚙️ Setup

### 1. Clone repository

```bash
git clone https://github.com/<your-username>/<repo>.git
cd homelab-git
```

### 2. Create environment file

```bash
cp stacks/.env.example /opt/media-stack/.env
```

Edit values if needed:

```bash
nano /opt/media-stack/.env
```

---

### 3. Run services

```bash
cd /opt/media-stack
docker compose up -d
```

---

## 📁 Project Structure

```
homelab-git/
├── stacks/
│   ├── media-stack.yml
│   └── .env.example
├── nginx/
├── web/
│   └── index.html
```

---

## 🔐 Security Notes

* `.env` is NOT included in this repository
* No secrets, tokens, or private keys are stored here
* This repo only contains configuration templates

---

## 🛠️ Tech Stack

* Docker & Docker Compose
* Nginx
* Ubuntu Server
* Cloudflare Tunnel (optional)
* Portainer (external)

---

## 📌 Notes

* Pi-hole is intentionally excluded from this repository due to configuration in the process
* Some system files are referenced via symlinks and may not be portable
* Adjust paths and ports according to your environment

---

## 📷 Preview

Landing page provides quick access to all services via a simple dashboard.

---

## 📄 License

This project is for personal use and learning purposes.
