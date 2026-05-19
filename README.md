<h5 align="center">‎𐂐 Adapted from <a href="https://github.com/Shineii86/MoeStickersBot">Shineii86/MoeStickersBot</a></h5>

> [!IMPORTANT]
> • **Use The Original Repository For Production**  
> • This Colab Notebook Is A **Personal Customization** Designed For Easy Testing And Short‑term Self‑hosting In Google Colab.  
> • For 24/7 Deployments, Contributions, Or Full Feature Support (Including WebApp), Please Refer To The [Original MoeStickersBot Repository](https://github.com/Shineii86/MoeStickersBot).

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go Version](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![Original Repo](https://img.shields.io/badge/Original-Shineii86%2FMoeStickerBot-181717?style=flat&logo=github)](https://github.com/Shineii86/MoeStickersBot)

[![GitHub Stars](https://img.shields.io/github/stars/Shineii86/MoeStickersBot?style=for-the-badge&color=FFB6C1)](https://github.com/Shineii86/MoeStickersBot/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Shineii86/MoeStickersBot?style=for-the-badge&color=FF6B9D)](https://github.com/Shineii86/MoeStickersBot/fork)

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
- [📓 Choose Your Version](#-choose-your-version)
  - [Animated Colors](#-animated--colors)
- [✨ Features](#-features)
- [🛠️ Prerequisites](#️-prerequisites)
  - [🔐 Create a Telegram Bot Token](#-create-a-telegram-bot-token)
- [🚀 Quick Start](#-quick-start)
- [📚 Detailed Setup](#-detailed-setup)
  - [Step 1: Open in Colab](#step-1-open-in-colab)
  - [Step 2: Install Dependencies & Build](#step-2-install-dependencies--build)
  - [Step 3: Download Helper Scripts](#step-3-download-helper-scripts)
  - [Step 4: Configure & Launch](#step-4-configure--launch)
- [🌐 Optional: Enable WebApp (ngrok)](#-optional-enable-webapp-ngrok)
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
- 🛠️ **Manage** stickers with a beautiful drag‑and‑drop WebApp *(optional)*
- 💾 **Download** Telegram stickers in multiple formats (PNG, WebP, GIF, WEBM)

This **Google Colab Edition** packages the entire setup into a single notebook. It installs all dependencies, compiles the bot from source, and launches it in the background — no VPS or Docker required. Perfect for testing, personal use, or just having fun with stickers.

> [!NOTE]
>  Free Colab sessions disconnect after ~90 minutes of inactivity. For 24/7 hosting, consider a VPS or the official Docker image.

---

## 📓 Choose Your Version

Pick the notebook that fits your style:

### Animated Colors

- 🎨 Full ANSI color support with background highlights
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ Animated braille spinners during long steps
- 💬 Clean, modern output with success/error/warning badges
- ✨ Best balance of style and readability

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBot.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-Animated%20Colors-FF6B9D?style=for-the-badge&logo=googlecolab" alt="Open v2 in Colab">
  </a>
</p>

---

### 💡 Pro Tip: Keep Colab Running Longer

Google Colab disconnects after ~90 minutes of inactivity. To maximize uptime without paying:

1. **Minimize the Colab widget** – Click the **< >** button (bottom‑left) to collapse the code/output panel. The session stays active while minimized.
2. **Keep the browser tab open** – Don't close it; you can switch to other tabs.
3. **Occasionally interact** – Scroll or click inside the notebook every 30‑45 minutes.

> For 24/7 operation, consider upgrading to **Colab Pro** (longer runtimes) or deploying on a free VPS (e.g., Oracle Cloud Always Free).

---

## ✨ Features

| Category | Feature | Description |
|----------|---------|-------------|
| 📥 **Import** | LINE Stickers | Import static, animated, emoji, and message stickers from LINE |
| | KakaoTalk Stickers | Import and decrypt Kakao emoticons, including animated ones |
| 🎨 **Creation** | Custom Packs | Build your own sticker sets from images/videos (any format) |
| | Animated Stickers | Convert videos to Telegram‑compatible WebM stickers |
| | Mixed Formats | Combine static and animated stickers in the same set |
| 🛠️ **Management** | WebApp Interface | Drag‑and‑drop reorder, edit emoji, add/remove stickers *(optional)* |
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
# 4. (Optional) Enable WebApp and add your ngrok auth token
# 5. Run the Launch cell
# 6. Open Telegram and send /start to your bot
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
└── /content/MoeStickersBot/MoeStickersBot
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

The Configuration cell contains all settings you can adjust. At minimum, enter your `BOT_TOKEN`. After configuring, run the **Launch** cell.

---

## 🌐 Optional: Enable WebApp (ngrok)

The WebApp manager requires a public HTTPS URL, which Colab doesn't provide natively. The notebook includes built‑in support for **ngrok** to create a secure tunnel.

### How to Enable

1. **Sign up for a free ngrok account** at [ngrok.com](https://ngrok.com/).
2. Copy your **authtoken** from the [dashboard](https://dashboard.ngrok.com/auth).
3. In the **Configuration** cell:
   - Set `ENABLE_WEBAPP = True`
   - Paste your token into `NGROK_AUTHTOKEN`
   - (Optional) Change `WEBAPP_PORT` if needed
4. Run all cells. The notebook will automatically:
   - Download and install ngrok
   - Start a tunnel to the WebApp port
   - Retrieve the public `https://` URL
   - Pass it to the bot via `--webapp_url`

> [!NOTE]
> Free ngrok URLs are temporary and change each session. You'll need to re‑run the setup if the Colab runtime restarts.

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
| `/manage` | Open the WebApp manager for your sticker sets *(requires WebApp enabled)* |
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

The notebook provides the following configuration options:

| Field | Required | Description |
|-------|----------|-------------|
| `BOT_TOKEN` | ✅ Yes | Your Telegram Bot Token |
| `ENABLE_DB` | ❌ No | Enable MariaDB for shared sticker sets |
| `DB_ADDR` / `DB_USER` / `DB_PASS` | Only if DB enabled | Database connection details |
| `ENABLE_WEBAPP` | ❌ No | Enable WebApp support via ngrok |
| `WEBAPP_PORT` | Only if WebApp | Port for internal WebApp server (default: 8080) |
| `NGROK_AUTHTOKEN` | Only if WebApp | Your free ngrok authtoken |
| `DATA_DIR` | ❌ No | Where the bot stores data |
| `LOG_LEVEL` | ❌ No | `debug`, `info`, `warn`, or `error` |
| `HTTP_PROXY` | ❌ No | Proxy URL if needed |

---

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| **"Bot exited immediately"** | Check `bot_stderr.log`. Common cause: invalid token format. |
| **Missing exiv2 warning** | Re‑run the dependency cell: `!apt-get install -y exiv2` |
| **Bot stops after ~90 minutes** | This is normal on free Colab. Keep the tab active, or use Colab Pro. |
| **WebApp not working** | Ensure `ENABLE_WEBAPP = True` and a valid `NGROK_AUTHTOKEN` is provided. |
| **ngrok URL not retrieved** | Check that your ngrok auth token is correct and that port `4040` isn't blocked. |
| **"Database not enabled" warning** | This is fine — the bot works fully without a database. |

For more detailed logs, set `LOG_LEVEL = "debug"` in the Configuration cell.

---

## ❓ FAQ

### Q: Is this Really Free?
> **A:** Yes! Google Colab is free, ngrok offers a free tier, and the bot is open‑source.

### Q: Can I Keep It Running 24/7?
> **A:** Free Colab sessions disconnect after inactivity. For permanent hosting, consider a VPS or the official Docker image.

### Q: Do I Need The Webapp?
> **A:** No, it's completely optional. The bot works perfectly without it; only the drag‑and‑drop sticker management feature requires the WebApp.

### Q: Can I Use My Own Custom Stickers?
> **A:** Absolutely! Send any image or video to the bot, and it will guide you through cropping, resizing, and converting.

### Q: Does It Support Animated Stickers?
> **A:** Yes! The bot converts videos to WebM format and supports both static and animated stickers in the same pack.

---

## 📄 License & Disclaimer

This Colab notebook is a convenience wrapper for **MoeStickersBot**, which is licensed under the **GNU General Public License v3.0 (GPL‑3.0)**.

> [!WARNING]
> **Disclaimer**: This notebook uses your personal Telegram Bot Token and (optionally) ngrok auth token. You are responsible for keeping them secure. The authors are not liable for any misuse or accidental exposure.

---

## 💕 Credits & Acknowledgments

### 🌟 Original Project

This notebook is built upon the incredible work of **[Star-39](https://github.com/Star-39)** and all contributors to **[MoeStickersBot](https://github.com/Shineii86/MoeStickersBot)**. Please show them some love!

### 📓 Colab Notebook Author

The Google Colab adaptation was crafted with ❤️ by **[Shinei Nouzen](https://github.com/Shineii86)**.  
If you find this notebook helpful, consider giving it a ⭐ and following for more Colab projects!

### 🛠️ Tools & Libraries

- [MoeStickersBot](https://github.com/Shineii86/MoeStickersBot) — The core Telegram bot (Go)
- [ImageMagick](https://imagemagick.org/) — Image processing
- [ffmpeg](https://ffmpeg.org/) — Video conversion
- [exiv2](https://exiv2.org/) — Metadata handling
- [ngrok](https://ngrok.com/) — Secure tunnel for WebApp
- [Google Colab](https://colab.research.google.com/) — Free cloud runtime
- [tqdm](https://github.com/tqdm/tqdm) — Progress bars

---

<div align="center">

### 💕 Support the Projects

⭐ **[Give a star to Shineii86/MoeStickersBot](https://github.com/Shineii86/MoeStickersBot)**  
⭐ **[Give a star to this Colab notebook](https://github.com/Shineii86/MoeStickerBot)**

<br>

<a href="https://github.com/Shineii86">
  <img src="https://img.shields.io/badge/Follow-@Shineii86-181717?style=for-the-badge&logo=github" alt="Follow Shineii86">
</a>
<a href="https://telegram.me/Shineii86">
  <img src="https://img.shields.io/badge/Telegram-@Shineii86-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram">
</a>

<img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=gradient&fontAlignY=30&section=footer">

<sup><b>Original Bot Copyright © Star-39 and contributors. GPL‑3.0 License.<br>Colab Adaptation © Shinei Nouzen. All Rights Reserved.</b></sup>

</div>
