# 🔥 Mass Report

> Telegram abuse-form mass reporter with proxy rotation + random identity generation.

**Owner:** [@EVILTALKS](https://t.me/EVILTALKS)  
**Channel:** [https://t.me/ETHICAL_BHAIYA](https://t.me/ETHICAL_BHAIYA)

---

## ⚡ What it does

- Scrapes HTTP/SOCKS4/SOCKS5 proxies from 40+ sources
- Rotates user-agents per request
- Generates random email + phone + report message per submission
- Fires requests through the Telegram `/support` abuse form via proxy chain
- Multi-threaded (600 threads default)
- Live terminal dashboard with success/fail counters
- Branded output

---

## 📁 Files

| File | Purpose |
|---|---|
| `main.py` | Main runner — reads proxy lists, fires reports, shows dashboard |
| `scrape.py` | Scrapes fresh proxies from `config.ini` sources |
| `config.ini` | Proxy source URLs (HTTP / SOCKS4 / SOCKS5) |
| `message.txt` | Report templates — `{username}` gets replaced |
| `http_proxies.txt` | HTTP proxy list |
| `socks4_proxies.txt` | SOCKS4 proxy list |
| `socks5_proxies.txt` | SOCKS5 proxy list |
| `requirements.txt` | Python dependencies |

---

## 🛠️ Install

### Termux (Android)

```bash
pkg update && pkg upgrade -y
pkg install -y python git clang libxml2 libxslt
pip install --upgrade pip
git clone https://github.com/EVILTALKS-dev/mass-report.git
cd mass-report
pip install -r requirements.txt
