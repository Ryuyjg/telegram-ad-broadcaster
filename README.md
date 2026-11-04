# 🤖 Telegram Ad Broadcaster & Session Manager

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.9+" />
  <img src="https://img.shields.io/badge/Telethon-Asyncio-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telethon" />
  <img src="https://img.shields.io/badge/Architecture-Master--Worker-orange?style=for-the-badge" alt="Architecture" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License" />
</div>

<p align="center">
  A high-throughput, multi-account Telegram advertising and audience broadcasting automation system built with asynchronous concurrency and distributed worker pools.
</p>

---

## ⚡ Core Architecture

- **🎮 Master Controller (`orbit_master.py`)**: Central management bot handling user authentication, campaign scheduling, session authorization, and worker orchestration.
- **⚙️ Parallel Worker Engine (`ad_worker.py`)**: Asynchronous worker processes that execute scheduled broadcasting sequences across multiple client sessions without blocking.
- **🔐 Session Pool Isolation**: Telethon StringSession support allowing isolated accounts to operate independently with automated rate-limit avoidance and delay jitter.
- **🛡️ Access Control**: JSON-backed user whitelist and administrative privilege enforcement.

---

## 🛠️ Tech Stack

- **Language**: Python 3.9+
- **Telegram Client API**: [Telethon](https://github.com/LonamiWebs/Telethon) (MTProto client)
- **Concurrency**: Asynchronous I/O (`asyncio`)
- **Terminal UI**: `colorama`

---

## 🚀 Quick Start

### 1. Prerequisites
- Python 3.9 or higher
- Telegram API Credentials (`api_id` and `api_hash` from [my.telegram.org](https://my.telegram.org))

### 2. Installation

```bash
# Clone the repository
git clone https://github.com/Ryuyjg/telegram-ad-broadcaster.git
cd telegram-ad-broadcaster

# Install requirements
pip install telethon colorama
```

### 3. Configuration
Add your credentials in `config.json`:
```json
{
  "api_id": 1234567,
  "api_hash": "your_api_hash_here",
  "bot_token": "your_bot_token_here"
}
```

### 4. Running the System

```bash
# Start the central controller bot
python orbit_master.py
```

---

## 👨‍💻 Author

- **Muhammad Ansif** ([@Ryuyjg](https://github.com/Ryuyjg))
