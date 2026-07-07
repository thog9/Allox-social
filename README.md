# Xeffy Bot Scripts 🚀

This collection of Python scripts automates tasks on the [AlloX](https://app.allox.ai?r=b04cf5) platform — an AI-powered crypto portfolio platform where users earn points by completing social tasks, daily check-ins, Twitter/X account linking, and welcome bonus claims.

🔗 Register: [AlloX](https://app.allox.ai?r=b04cf5)

---

## ✨ Features Overview

### General Features

- **Multi-Account Support**: Reads private keys from `pvkey.txt` to process multiple wallets in parallel.
- **Central Menu System**: Interactive menu for easy script selection via `main.py`.
- **Colorful CLI**: Uses `colorama` for visually appealing output with box-drawing borders and colored icons.
- **Asynchronous Execution**: Built with `asyncio` for efficient concurrent task processing.
- **Error Handling**: Comprehensive error catching with retry logic for API failures.
- **Bilingual Support**: Supports both English and Vietnamese output.
- **Proxy Support**: Supports HTTP, HTTPS, and SOCKS5 proxies via `proxies.txt`.

---

### Included Scripts

✨ **Welcome Bonus** (`bonus.py`)

- ✅ One-time Season 1 claim (5000 pts)
- ✅ Checks already-claimed status via `/auth/me`
- ✅ Displays on-chain balance snapshot after claiming
- ✅ Multi-account parallel execution
- ✅ Proxy support

✨ **Auto Check-in Daily** (`checkin.py`)

- ✅ Daily on-chain check-in on BNB Chain or Base
- ✅ Sends check-in transaction via smart contract
- ✅ Verifies with `/checkin` + `/checkin/reconcile`
- ✅ Checks already-checked status to avoid duplicates
- ✅ Explorer link display after successful tx
- ✅ Multi-account support
- ✅ Proxy support

✨ **Connect Twitter** (`connect.py`)

- ✅ X (Twitter) account linking via OAuth
- ✅ Checks existing connection status before flow
- ✅ Auto-approve with token from `tokenX.txt`
- ✅ Manual fallback mode (opens browser)
- ✅ Username display after successful connection
- ✅ Multi-account parallel execution
- ✅ Proxy support

✨ **Auto Twitter Tasks** (`socialX.py`)

- ✅ Verify follow @alloxdotai (+1000 pts)
- ✅ Verify promo tweet (+500 pts)
- ✅ Auto like/retweet tweet tasks
- ✅ Fetches task list from `/twitter/tasks`
- ✅ Displays total social points earned
- ✅ Multi-account support
- ✅ Proxy support

---

## 🛠️ Prerequisites

Before running the scripts, ensure you have the following installed:

- **Python 3.10+**
- **pip** (Python package manager)
- **Dependencies**: Install via `pip install -r requirements.txt`
- **pvkey.txt**: Add EVM private keys (one per line) — with `0x` prefix or without
- **proxies.txt** (optional): Add proxy addresses for network requests
- **tokenX.txt** (optional): Add Twitter auth tokens for auto OAuth (`auth_token|ct0` per line)

---

## 📦 Installation

1. **Clone or download this repository:**
   ```sh
   git clone https://github.com/thog9/Allox-social.git
   cd Allox-social
   ```

2. **Install Dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Prepare Input Files:**

   Create `pvkey.txt` in the root directory with EVM private keys (one per line):
   ```
   0x999
   0x999
   ```

   Create `proxies.txt` (optional) — one proxy per line:
   ```
   http://user:pass@ip:port
   socks5://user:pass@ip:port
   ip:port:user:pass
   ```

   Create `tokenX.txt` (optional for connect.py) — Twitter auth token and ct0 per line:
   ```
   auth_token_value|ct0_value
   ```

4. **Run:**
   ```sh
   python main.py
   ```
   - Choose a language (Vietnamese / English).
   - Select the script you want to run.

**Language Selection:**
- Choose between Vietnamese (Tiếng Việt) and English.
- All scripts support bilingual output.

---

## 📁 Project Structure

```
Allox-social/
├── main.py                 # Central menu system
├── pvkey.txt               # EVM private keys
├── proxies.txt             # Proxies (optional)
├── tokenX.txt              # Twitter tokens (optional)
├── requirements.txt        # Python dependencies
├── README.md               # This file
└── scripts/                # Individual scripts
    ├── bonus.py            # Welcome Bonus (Season 1)
    ├── checkin.py          # Auto Check-in Daily
    ├── connect.py          # Twitter OAuth connection
    └── socialX.py          # Auto Twitter Tasks

```

---

## 📨 Contact

Connect with us for support or updates:

- **Telegram**: [thog099](https://t.me/thog099)
- **Channel**: [CHANNEL](https://t.me/thogairdrops)
- **Group**: [GROUP CHAT](https://t.me/thogchats)
- **X**: [Thog](https://x.com/thog099)

---

## ☕ Support Us

Love these scripts? Fuel our work with a coffee!

🔗 BUYMECAFE: [BUY ME CAFE](https://buymecafe.vercel.app/)

🔗 WEBSITE: [BUY SCRIPTS](https://thogtoolhub.com/)
