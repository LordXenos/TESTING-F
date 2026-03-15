<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Zero%20Bot&fontSize=70&fontColor=ffffff&fontAlignY=38&desc=Advanced%20Facebook%20Messenger%20Bot&descAlignY=60&descSize=20&animation=fadeIn" width="100%"/>

<br>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=A855F7&center=true&vCenter=true&width=600&lines=Facebook+Messenger+Bot;131%2B+Commands+%7C+Smart+AI;Role-Based+Access+Control;No+Google+Auth+Required;Built+by+乛+Xenos+ゎ" alt="Typing SVG"/>

<br><br>

[![Node.js](https://img.shields.io/badge/Node.js-20.x-43853d?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)
[![Platform](https://img.shields.io/badge/Platform-Facebook%20Messenger-1877f2?style=for-the-badge&logo=messenger&logoColor=white)](https://messenger.com)
[![Commands](https://img.shields.io/badge/Commands-131%2B-a855f7?style=for-the-badge&logo=bolt&logoColor=white)](#commands)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Author](https://img.shields.io/badge/Modified%20by-乛%20Xenos%20ゎ-f59e0b?style=for-the-badge&logo=github&logoColor=white)](https://github.com/NeoKEX)

</div>

---

<div align="center">

## ⚡ Bot Overview

</div>

```
╔══════════════════════════════════════════════════════════╗
║                    ZERO BOT  ♥️🎀                        ║
║══════════════════════════════════════════════════════════║
║  Name       │  Zero ♥️🎀                                 ║
║  Prefix     │  ,  (normal)   !!  (admin only)            ║
║  No-Prefix  │  Supported  (off / all / adminOnly)        ║
║  Commands   │  131+  across multiple categories          ║
║  Events     │  7  auto-loaded event scripts              ║
║  Language   │  English / Vietnamese                      ║
║  Timezone   │  Asia/Dhaka                                ║
║  Database   │  SQLite  (MongoDB supported)               ║
║  Dashboard  │  Web UI  (Express + Socket.io)             ║
╚══════════════════════════════════════════════════════════╝
```

---

<div align="center">

## 🎭 Permission System

</div>

<div align="center">

| Tier | Role | Access Level | Description |
|:----:|------|:------------:|-------------|
| 🔴 `4` | **Developer** | Full Access | Shell, eval, all commands, admin prefix |
| 🟠 `2` | **Bot Admin** | High | System commands, admin prefix, noprefix |
| 🟡 `3` | **Premium User** | Medium-High | Premium & normal commands only |
| 🟢 `1` | **Group Admin** | Medium | Group-level management commands |
| ⚪ `0` | **User** | Standard | Public commands |

</div>

---

<div align="center">

## 🚀 Core Features

</div>

<table>
<tr>
<td width="50%">

### 🔐 Dual Prefix System
- **Normal prefix** `,` — everyone
- **Admin prefix** `!!` — role 2+ only
- Per-thread custom prefix supported
- Change anytime via `,prefix` command

### 🪄 No-Prefix Mode
- `off` → disabled
- `on` → all users can call commands without prefix
- `only admin` → only admins/devs
- Ignores regular chat — only responds to real command names

### 🤖 Smart Command Suggestions
- Typo detection using edit-distance algorithm
- Shows **up to 3 closest matches** when a command isn't found
- Prefix-aware suggestions (shows correct prefix used)

</td>
<td width="50%">

### 🛡️ Anti-Spam Protection
- Auto-ban threads that spam commands
- Configurable threshold, time window & ban duration
- Auto-expire and auto-unban system

### 💰 Premium & Economy
- Money-based premium system
- Per-command money requirements
- Premium users (role 3) get exclusive access

### 🌐 Web Dashboard
- Manage threads, users, settings via browser
- Real-time stats via Socket.io
- Secure login with expire-based verify codes

</td>
</tr>
</table>

---

<div align="center">

## 📦 System Architecture

</div>

```
Zero Bot
├── bot/
│   ├── handler/
│   │   └── handlerEvents.js     ← Core message router & command engine
│   └── login/
│       └── login.js             ← Facebook auth & session management
├── scripts/
│   ├── cmds/                    ← 131+ command scripts
│   └── events/                  ← 7 event listener scripts
├── languages/
│   ├── en.lang                  ← English language strings
│   └── vi.lang                  ← Vietnamese language strings
├── dashboard/                   ← Web UI (Express)
├── fca-sifu/                    ← Facebook Chat API (no Google auth)
│   └── data/                    ← Internal FCA database
└── config.json                  ← Main configuration file
```

---

<div align="center">

## ⚙️ Configuration

</div>

```json
{
  "prefix": ",",
  "adminPrefix": "!!",
  "noPrefix": false,
  "language": "en",
  "timeZone": "Asia/Dhaka",

  "adminBot": ["YOUR_FACEBOOK_ID"],
  "devUsers": ["YOUR_FACEBOOK_ID"],
  "premiumUsers": [],

  "whiteListMode": {
    "enable": false,
    "whiteListIds": []
  },

  "database": {
    "type": "sqlite"
  },

  "dashBoard": {
    "enable": true,
    "port": 5000
  }
}
```

### 🔑 Key Config Options

| Key | Values | Description |
|-----|--------|-------------|
| `prefix` | any string | Normal command prefix |
| `adminPrefix` | any string | Admin-only prefix (role 2+) |
| `noPrefix` | `false` / `true` / `"adminOnly"` | No-prefix mode control |
| `adminBot` | `["uid"]` | Bot admins (role 2) |
| `devUsers` | `["uid"]` | Developers (role 4) |
| `premiumUsers` | `["uid"]` | Premium users (role 3) |

---

<div align="center">

## 🛠️ Installation

</div>

### 1. Clone & Install

```bash
git clone https://github.com/ntkhang03/Goat-Bot-V2.git
cd Goat-Bot-V2
npm install
```

### 2. Add Your Cookie

Put your Facebook account cookie into `account.txt` (appstate format).

> ⚠️ **Always use a secondary/clone Facebook account. Never your main.**

### 3. Configure

Edit `config.json` — set your user ID in `adminBot` and `devUsers`.

### 4. Start

```bash
npm start
```

---

<div align="center">

## ☁️ Deploy Options

</div>

<div align="center">

| Platform | Cost | Notes |
|----------|------|-------|
| **Replit** | Free | Quick setup, recommended for testing |
| **Render** | Free tier | Auto-deploy from GitHub |
| **Railway** | $5/mo credit | Best for 24/7 uptime |
| **VPS** | Varies | Full control, use PM2 |

</div>

---

<div align="center">

## 📋 Prefix System Summary

</div>

```
Normal Users    →   ,help   ,ai   ,pfp   etc.
Bot Admin/Dev   →   ,help   OR   !!help  (both work)
No-Prefix ON    →   help    ai    pfp    (no prefix needed)
No-Prefix Admin →   only admin/dev can use without prefix
```

---

<div align="center">

## 💻 Command Categories

</div>

<details>
<summary><b>📂 View all categories</b></summary>

<br>

| Category | Description |
|----------|-------------|
| `system` | Bot management — prefix, noprefix, reload, eval, shell |
| `ai` | AI chat, image generation, GPT |
| `media` | Profile picture, images, videos |
| `game` | Mini-games and fun commands |
| `economy` | Money, shop, daily rewards |
| `social` | Rank, level, profile |
| `utility` | Weather, translate, calc, wiki |
| `admin` | Ban, unban, whitelist, thread control |
| `fun` | Memes, random, entertainment |

</details>

---

<div align="center">

## 📊 Stats

</div>

<div align="center">

```
┌─────────────────────────────────────────┐
│   Commands Loaded    │       131+        │
│   Event Scripts      │        7          │
│   Supported DB       │  SQLite / MongoDB │
│   API               │  FCA-SIFU (v1)    │
│   Auth Method        │  Cookie (No OAuth)│
│   Node Version       │  v20.x            │
└─────────────────────────────────────────┘
```

</div>

---

<div align="center">

## 🧠 How It Works

</div>

```
Message received
      │
      ▼
  Check prefix? ──── normal prefix (,) ────► parse & run command
      │
      ├── admin prefix (!!) ──── role >= 2? ──► parse & run command
      │
      ├── noprefix ON ────── first word = command? ──► run command
      │                         role check if adminOnly
      │
      └── none match ──► ignore silently


Command execution flow:
  1. Check spam ban (thread)
  2. Check user ban
  3. Check adminOnly mode
  4. Check money requirement
  5. Check role permission
  6. Check cooldown
  7. Execute → log
```

---

<div align="center">

## 📸 Screenshots

</div>

<details>
<summary><b>🎮 Bot in Action</b></summary>

- Rank card:
  <p><img src="https://i.ibb.co/d0JDJxF/rank.png" width="399px"></p>

- Rankup notification:
  <p><img src="https://i.ibb.co/WgZzthH/rankup.png" width="399px"></p>

- AI / GPT:
  <p><img src="https://i.ibb.co/D4wRbM3/Screenshot-2023-05-09-22-47-48-037-com-facebook-orca.jpg" width="399px"></p>

- Weather:
  <p><img src="https://i.ibb.co/2FwWVLv/weather.png" width="399px"></p>

</details>

<details>
<summary><b>🖥️ Dashboard</b></summary>

- Home:
  <p><img src="https://i.postimg.cc/GtwP4Cqm/Screenshot-2023-12-23-105357.png" width="399px"></p>

- Thread Manager:
  <p><img src="https://i.postimg.cc/RF237v1Z/Screenshot-2023-12-23-105913.png" width="399px"></p>

- Custom Welcome:
  <p><img src="https://i.ibb.co/6ZrQqc1/image.png" width="399px"></p>

</details>

---

<div align="center">

## 📜 License & Rules

</div>

> **If you violate any rule, you will be banned from using this project.**

- Do **not** sell this source code
- Do **not** claim ownership of this source code
- Do **not** monetize (selling commands, bots, donations) using this code
- Do **not** remove or modify credits in the source

---

<div align="center">

## 👥 Credits

</div>

<div align="center">

| Role | Name | GitHub |
|------|------|--------|
| Original Author | **NTKhang** | [@ntkhang03](https://github.com/ntkhang03) |
| Modified & Enhanced | **乛 Xenos ゎ** | [@NeoKEX](https://github.com/NeoKEX) |
| FCA Library | **FCA-SIFU** | [@LordXenos](https://github.com/LordXenos/FCA-SIFU) |

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer&animation=fadeIn" width="100%"/>

**Built with ♡ by 乛 Xenos ゎ**

*Zero Bot — Facebook Messenger Automation, Elevated.*

</div>
