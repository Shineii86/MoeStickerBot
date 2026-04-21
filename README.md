<h5 align="center">‎𐂐 Adapted from <a href="https://github.com/Star-39/Moe-Sticker-Bot">star-39/moe-sticker-bot</a></h5>

> [!IMPORTANT]
> • **Use The Original Repository For Production**  
> • This Colab notebook Is A **Personal Customization** Designed For Easy Testing And Short‑term Self‑hosting In Google Colab.  
> • For 24/7 Deployments, Contributions, Or Full Feature Support (Including WebApp), Please Refer To The [Original Moe-Sticker-Bot Repository](https://github.com/star-39/moe-sticker-bot).

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=&height=200&section=header&text=Moe%20Sticker%20Bot&fontSize=60&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Colab%20Edition%20—%20Self‑Host%20Your%20Telegram%20Sticker%20Bot&descSize=18" />

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Shineii86/moe-sticker-bot-colab/blob/main/notebooks/MeoStickerBot.ipynb)
[![Original Repo](https://img.shields.io/badge/Original-Star--39%2FMoe--Sticker--Bot-181717?style=flat&logo=github)](https://github.com/star-39/moe-sticker-bot)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go Version](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![GitHub Stars](https://img.shields.io/github/stars/star-39/moe-sticker-bot?style=for-the-badge&color=FFB6C1)](https://github.com/star-39/moe-sticker-bot/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/star-39/moe-sticker-bot?style=for-the-badge&color=FF6B9D)](https://github.com/star-39/moe-sticker-bot/fork)

**Import LINE & Kakao stickers to Telegram · Create custom sticker sets · Manage everything via WebApp — all running for free in Google Colab.**

</div>

---

<div align="center">

### 📢 Subscribe to My Telegram Sticker Channel!


<p align="center">
  <a href="https://t.me/MaximXStickers">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=dark">
      <source media="(prefers-color-scheme: light)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=light">
      <img src="https://telegramcard.vercel.app/?username=MaximXStickers&bgColor=rgba%28127%2C+29%2C+29%2C+1%29&textColor=%23fef2f2&subtleTextColor=%23fca5a5&extraColor=%23fbbf24&shadowColor=rgba%28251%2C+191%2C+36%2C+0.3%29&fontFamily=Arial%2C+sans-serif" alt="MaximXStickers Telegram Channel" width="850" />
    </picture>
  </a>
</p>

<i><p>Get daily sticker packs, updates, and exclusive content!</p></i>

</div>
<br>

---

## 📖 Table of Contents

- [🎯 Overview](#-overview)
- [✨ Features](#-features)
- [🛠️ Prerequisites](#️-prerequisites)
  - [🔐 Create a Telegram Bot Token](#-create-a-telegram-bot-token)
- [🚀 Quick Start](#-quick-start)
- [📚 Detailed Setup](#-detailed-setup)
  - [Step 1: Open in Colab](#step-1-open-in-colab)
  - [Step 2: Install Dependencies & Build](#step-2-install-dependencies--build)
  - [Step 3: Download Helper Scripts](#step-3-download-helper-scripts)
  - [Step 4: Configure & Launch](#step-4-configure--launch)
- [🤖 Bot Commands](#-bot-commands)
- [⚙️ Configuration Reference](#️-configuration-reference)
- [🔧 Troubleshooting](#-troubleshooting)
- [❓ FAQ](#-faq)
- [📄 License & Disclaimer](#-license--disclaimer)
- [💕 Credits & Acknowledgments](#-credits--acknowledgments)

---

## 🎯 Overview

**Moe Sticker Bot** is a powerful Telegram bot written in Go that lets you:

- 📥 **Import** LINE and KakaoTalk sticker packs directly into Telegram
- 🎨 **Create** your own sticker sets from any image or video
- 🛠️ **Manage** stickers with a beautiful drag‑and‑drop WebApp
- 💾 **Download** Telegram stickers in multiple formats (PNG, WebP, GIF, WEBM)

This **Google Colab Edition** packages the entire setup into a single notebook. It installs all dependencies, compiles the bot from source, and launches it in the background — no VPS or Docker required. Perfect for testing, personal use, or just having fun with stickers.

> [!NOTE]
>  Free Colab sessions disconnect after ~90 minutes of inactivity. For 24/7 hosting, consider a VPS or the official Docker image.

---

## ✨ Features

| Category | Feature | Description |
|----------|---------|-------------|
| 📥 **Import** | LINE Stickers | Import static, animated, emoji, and message stickers from LINE |
| | KakaoTalk Stickers | Import and decrypt Kakao emoticons, including animated ones |
| 🎨 **Creation** | Custom Packs | Build your own sticker sets from images/videos (any format) |
| | Animated Stickers | Convert videos to Telegram‑compatible WebM stickers |
| | Mixed Formats | Combine static and animated stickers in the same set |
| 🛠️ **Management** | WebApp Interface | Drag‑and‑drop reorder, edit emoji, add/remove stickers |
| | Edit Titles | Rename existing sticker sets |
| 💾 **Download** | Batch Export | Download entire sticker sets as ZIP archives |
| | Format Conversion | Convert stickers to PNG, WebP, GIF, or original format |
| 🔍 **Search** | Database Search | Find previously imported sticker packs |
| ⚡ **Performance** | Multi‑threaded | Goroutines and worker pools for fast processing |

---

## 🛠️ Prerequisites

You only need two things:

1. **A Google Account** (for Colab)
2. **A Telegram Bot Token** (from [@BotFather](https://t.me/BotFather))

### 🔐 Create a Telegram Bot Token

1. Open Telegram and search for **@BotFather**.
2. Send the command `/newbot`.
3. Choose a **name** for your bot (e.g., `My Sticker Bot`).
4. Choose a **username** ending in `bot` (e.g., `my_sticker_bot`).
5. BotFather will give you a token like:
   ```
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
   ```
6. **Copy this token** — you'll need it in the Configuration step.

> 🔒 **Keep your token secret!** Anyone with it can control your bot.

---

## 🚀 Quick Start

```bash
# 1. Click the "Open in Colab" badge above
# 2. Run all cells (Runtime → Run all)
# 3. In the Configuration cell, paste your Bot Token
# 4. Run the Launch cell
# 5. Open Telegram and send /start to your bot
```

That's it! The notebook handles everything else: installing Go, system tools, Python helpers, and compiling the bot.

---

## 📚 Detailed Setup

### Step 1: Open in Colab

Click the **"Open in Colab"** badge at the top of this README. This will load the notebook into your Google Colab environment.

### Step 2: Install Dependencies & Build

The first code cell installs all required system packages and compiles the bot.

**What gets installed:**

```
System Packages:
├── imagemagick          → Image processing
├── ffmpeg               → Video/animation conversion
├── libarchive-tools     → Archive extraction (bsdtar)
├── curl, gifsicle       → Network & GIF tools
├── python3              → For helper scripts
└── exiv2                → Metadata handling

Go Compiler:
└── go1.21.5             → Go programming language

Build Output:
└── /content/moe-sticker-bot/moe-sticker-bot
```

**Expected output:**
```
✅ All system dependencies installed!
Go version: go1.21.5
exiv2 version: 0.27.3
ffmpeg version: 4.4.2
ImageMagick version: 6.9.11
```

### Step 3: Download Helper Scripts

The second cell downloads Python helper scripts that the bot uses for specialized tasks:

| Script | Purpose |
|--------|---------|
| `msb_emoji.py` | Extract and assign emoji representations |
| `msb_kakao_decrypt.py` | Decrypt animated KakaoTalk stickers |
| `msb_rlottie.py` | Convert TGS (Telegram animated sticker) format |

These are placed in `/usr/local/bin/` so the bot can find them.

### Step 4: Configure & Launch

The Configuration cell contains all settings you can adjust:

| Field | Required | Description |
|-------|----------|-------------|
| `BOT_TOKEN` | ✅ Yes | Your Telegram Bot Token |
| `ENABLE_DB` | ❌ No | Enable MariaDB for shared sticker sets |
| `DB_ADDR` / `DB_USER` / `DB_PASS` | Only if DB enabled | Database connection details |
| `DATA_DIR` | ❌ No | Where the bot stores data (default: `moe_sticker_bot_data`) |
| `LOG_LEVEL` | ❌ No | `debug`, `info`, `warn`, or `error` |
| `HTTP_PROXY` | ❌ No | Proxy URL if needed |

After entering your token, run the **Launch** cell. The bot will start in the background, and you'll see:

```
✅ Bot launched!
   • PID: 12345
   • Logs: bot_stdout.log, bot_stderr.log
✅ Bot is RUNNING and connected to Telegram!
📱 Go to Telegram and send /start to your bot!
```

---

## 🤖 Bot Commands

Once running, interact with your bot on Telegram using these commands:

| Command | Description |
|---------|-------------|
| `/start` | Welcome message and basic instructions |
| `/help` | Show all available commands |
| `/import` | Import a LINE or Kakao sticker pack from a share link |
| `/search` | Search for previously imported sticker sets |
| `/create` | Create a new sticker set from your own images/videos |
| `/manage` | Open the WebApp manager for your sticker sets |
| `/download` | Download Telegram stickers or GIFs |
| `/crop` | Crop an image before making it a sticker |
| `/resize` | Resize an image |
| `/addtext` | Add custom text to a sticker |
| `/emoji` | Add an emoji overlay |
| `/convert` | Convert to WebM (animated) |
| `/delete` | Delete a sticker set you own |

> 💡 **Tip**: You can also just send a **LINE/Kakao sticker link** directly to the bot — it will automatically offer to import it.

---

## ⚙️ Configuration Reference

The bot accepts these command‑line flags (automatically built by the notebook):

| Flag | Description | Default |
|------|-------------|---------|
| `--bot_token` | **Required.** Telegram Bot Token | *(none)* |
| `--data_dir` | Working directory for bot data | `moe_sticker_bot_data` |
| `--log_level` | Logging verbosity | `info` |
| `--db_addr` | MariaDB server address (host:port) | *(empty)* |
| `--db_user` | Database username | *(empty)* |
| `--db_pass` | Database password | *(empty)* |
| `--db_name` | Database name | `moe_sticker_bot` |
| `--http_proxy` | HTTP proxy URL | *(empty)* |

---

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| **"Bot exited immediately"** | Check `bot_stderr.log`. Common cause: invalid token format. |
| **Missing exiv2 warning** | Re‑run the dependency cell: `!apt-get install -y exiv2` |
| **Bot stops after ~90 minutes** | This is normal on free Colab. Keep the tab active, or use Colab Pro. |
| **Sticker conversion fails** | Ensure `ffmpeg` and `ImageMagick` are installed. Re‑run the first cell. |
| **WebApp not working** | WebApp requires a public HTTPS URL. It's disabled by default on Colab. |
| **"Database not enabled" warning** | This is fine — the bot works fully without a database. |

For more detailed logs, set `LOG_LEVEL = "debug"` in the Configuration cell.

---

## ❓ FAQ

### Q: Is this really free?
**A:** Yes! Google Colab is free, and the bot is open‑source. You only need a Telegram account.

### Q: Can I keep it running 24/7?
**A:** Free Colab sessions disconnect after inactivity. For permanent hosting, consider:
- Colab Pro (up to 24‑hour runtimes)
- A cheap VPS (Oracle Cloud free tier works great)
- The official Docker container

### Q: Do I need a database?
**A:** No. The database is only required for the shared sticker set feature. For personal use, everything works without it.

### Q: Can I use my own custom stickers?
**A:** Absolutely! Send any image or video to the bot, and it will guide you through cropping, resizing, and converting.

### Q: Does it support animated stickers?
**A:** Yes! The bot converts videos to WebM format and supports both static and animated stickers in the same pack.

---

## 📄 License & Disclaimer

This Colab notebook is a convenience wrapper for **moe-sticker-bot**, which is licensed under the **GNU General Public License v3.0 (GPL‑3.0)**.

> ⚠️ **Disclaimer**: This notebook uses your personal Telegram Bot Token. You are responsible for keeping it secure. The authors are not liable for any misuse or accidental exposure.

---

## 💕 Credits & Acknowledgments

### 🌟 Original Project

This notebook is built upon the incredible work of **[star-39](https://github.com/star-39)** and all contributors to **[moe-sticker-bot](https://github.com/star-39/moe-sticker-bot)**. Please show them some love!

### 📓 Colab Notebook Author

The Google Colab adaptation was crafted with ❤️ by **[Shinei Nouzen](https://github.com/Shineii86)**.  
If you find this notebook helpful, consider giving it a ⭐ and following for more Colab projects!

### 🛠️ Tools & Libraries

- [moe-sticker-bot](https://github.com/star-39/moe-sticker-bot) — The core Telegram bot (Go)
- [ImageMagick](https://imagemagick.org/) — Image processing
- [ffmpeg](https://ffmpeg.org/) — Video conversion
- [exiv2](https://exiv2.org/) — Metadata handling
- [Google Colab](https://colab.research.google.com/) — Free cloud runtime
- [tqdm](https://github.com/tqdm/tqdm) — Progress bars

---

<div align="center">

### 💕 Support the Projects

⭐ **[Give a star to star-39/moe-sticker-bot](https://github.com/star-39/moe-sticker-bot)**  
⭐ **[Give a star to this Colab notebook](https://github.com/Shineii86/moe-sticker-bot-colab)**

<br>

<a href="https://github.com/Shineii86">
  <img src="https://img.shields.io/badge/Follow-@Shineii86-181717?style=for-the-badge&logo=github" alt="Follow Shineii86">
</a>
<a href="https://telegram.me/Shineii86">
  <img src="https://img.shields.io/badge/Telegram-@Shineii86-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram">
</a>

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=&height=100&section=footer" width="100%">

<sup><b>Original Bot Copyright © star-39 and contributors. GPL‑3.0 License.<br>Colab Adaptation © Shinei Nouzen. All Rights Reserved.</b></sup>

</div>
