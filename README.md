<h5 align="center">‎𐂐 Adapted from <a href="https://github.com/Shineii86/MoeStickersBot">Shineii86/MoeStickesBot</a></h5>

> [!IMPORTANT]
> • **Use The Original Repository For Production**  
> • This Colab Notebook Is A **Personal Customization** Designed For Easy Testing And Short‑term Self‑hosting In Google Colab.  
> • For 24/7 Deployments, Contributions, Or Full Feature Support (Including WebApp), Please Refer To The Original [Moe-Sticker-Bot](https://github.com/star-39/moe-sticker-bot) Repository.

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go Version](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

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
      <source media="(prefers-color-scheme: dark)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=dark&verified=true">
      <source media="(prefers-color-scheme: light)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&&theme=light&verified=true">
      <img src="https://telegramcard.vercel.app/?username=MaximXStickers&bgColor=rgba%28127%2C+29%2C+29%2C+1%29&textColor=%23fef2f2&subtleTextColor=%23fca5a5&extraColor=%23fbbf24&shadowColor=rgba%28251%2C+191%2C+36%2C+0.3%29&fontFamily=Arial%2C+sans-serif&verified=true" alt="Telegram Channel" width="850" />
    </picture>
  </a>
</p>

<i><p>Get daily sticker packs, updates, and exclusive content!</p></i>

</div>
<br>

---

## 📖 Table of Contents

- [🎯 Overview](#-overview)
- [📓 Notebook](#-notebook)
- [✨ Features](#-features)
- [🛠️ Prerequisites](#️-prerequisites)
  - [🔐 Create a Telegram Bot Token](#-create-a-telegram-bot-token)
- [🚀 Quick Start](#-quick-start)
- [📚 How It Works](#-how-it-works)
  - [⚙️ Configuration & Bot Token](#️-configuration--bot-token)
  - [📦 Dependencies & Build](#-dependencies--build)
  - [🚀 Launch & Auto-Restart](#-launch--auto-restart)
- [🌐 Optional: Enable WebApp (ngrok)](#-optional-enable-webapp-ngrok)
- [🔐 Owner-Only: Update Bot Token](#-owner-only-update-bot-token)
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

## 📓 Notebook

The setup is a single collapsible cell — code hidden by default, just hit play.

- 🎨 **Theme-adaptive colors** — auto-detects light/dark Colab mode
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ Animated braille spinners during long steps
- 💬 Colored status badges with timestamps (`HH:MM:SS`)
- 🔐 Encrypted bot token — no manual entry needed
- 💓 Keep-alive heartbeat to prevent Colab timeout
- 🔄 Auto-restart on crash (up to 5 attempts)
- 🐛 **Debug mode** — set `LOG_LEVEL = "debug"` for verbose output
- 🩺 Stderr capture on crash — shows actual Go errors, not generic messages
- 🔒 TiDB TLS auto-patch — enables encrypted DB connections

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBot.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-MoeStickerBot-FF6B9D?style=for-the-badge&logo=googlecolab" alt="Open in Colab">
  </a>
</p>

---

### 💡 Pro Tip: Keep Colab Running Longer

Google Colab disconnects after ~90 minutes of inactivity. The notebook has a built-in **keep-alive heartbeat** that prints every 10 minutes to help prevent timeouts. To maximize uptime:

1. **Keep the browser tab open** – Don't close it; you can switch to other tabs.
2. **Occasionally interact** – Scroll or click inside the notebook every 30‑45 minutes.
3. **The heartbeat does the rest** – It prints a timestamp every 10 min to keep the session alive.

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
| 🎨 **UI Engine** | Theme Detection | Auto-detects light/dark mode, adjusts all ANSI colors |
| | Timestamps | `HH:MM:SS` on every status message |
| | Debug Mode | Set `LOG_LEVEL="debug"` for detailed internal logs |
| | Log Highlighting | Color-coded log levels (INFO/WARN/ERR/FATAL/DEBUG) |

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
# 2. Click ▶ Play on the main cell (code is hidden — just the title shows)
# 3. When prompted, the bot uses a pre-configured encrypted token
# 4. (Optional) Edit ENABLE_WEBAPP & NGROK_AUTHTOKEN inside the cell
# 5. Open Telegram and send /start to your bot
```

That's it! The single cell handles everything: installing Go, system tools, Python helpers, compiling the bot, and launching it with auto-restart.

---

## 📚 How It Works

The entire bot setup lives in **one collapsible cell** with the title `🚀 Moe Sticker Bot — Configuration & Launch`. In Colab, the code is hidden by default — you only see the title and a play button. No input boxes, no editable fields.

### ⚙️ Configuration & Bot Token

All settings are defined at the top of the cell as Python variables:

```python
ENABLE_DB       = True        # TiDB Cloud shared database
ENABLE_WEBAPP   = False       # Set True to expose WebApp via ngrok
WEBAPP_PORT     = 8080
NGROK_AUTHTOKEN = ""          # Required if ENABLE_WEBAPP=True
DATA_DIR        = "moe_sticker_bot_data"
LOG_LEVEL       = "info"      # debug, info, warn, error
HTTP_PROXY      = ""          # Optional http://proxy:port
AUTO_RESTART    = True        # Auto-restart bot on crash
MAX_RESTARTS    = 5           # Max restart attempts
KEEP_ALIVE      = True        # Heartbeat every 10 min (fights Colab timeout)
```

The bot token is **encrypted** and embedded in the cell. You don't need to enter it manually. If you need to update it, use the **Owner-Only Token Tool** cell at the bottom of the notebook.

### 📦 Dependencies & Build

When you run the cell, it automatically:

1. **Installs system packages** — `imagemagick`, `ffmpeg`, `libarchive-tools`, `curl`, `gifsicle`, `python3`, `exiv2`
2. **Connects to TiDB Cloud** — shared database with TLS encryption
3. **Downloads Go 1.22.4** — compiles the bot from source
4. **Fetches Python helpers** — `msb_emoji.py`, `msb_kakao_decrypt.py`, `msb_rlottie.py`
5. **Clones, patches & builds** — downloads bot source, applies TLS fix, compiles binary

### 🚀 Launch & Auto-Restart

After building, the cell:

- Validates the bot token format
- Optionally starts an ngrok tunnel for WebApp
- Launches the bot as a subprocess
- Streams color-coded logs in real-time
- **Auto-restarts** on crash (up to 5 attempts)
- Sends a **keep-alive heartbeat** every 10 minutes to prevent Colab timeout

---

## 🌐 Optional: Enable WebApp (ngrok)

The WebApp manager requires a public HTTPS URL, which Colab doesn't provide natively. The notebook includes built‑in support for **ngrok** to create a secure tunnel.

### How to Enable

1. **Sign up for a free ngrok account** at [ngrok.com](https://ngrok.com/).
2. Copy your **authtoken** from the [dashboard](https://dashboard.ngrok.com/auth).
3. **Expand the main cell** by clicking its title, then edit the config variables:
   - Set `ENABLE_WEBAPP = True`
   - Set `NGROK_AUTHTOKEN = "your_token_here"`
   - (Optional) Change `WEBAPP_PORT` if needed
4. Run the cell. It will automatically:
   - Download and install ngrok
   - Start a tunnel to the WebApp port
   - Retrieve the public `https://` URL
   - Pass it to the bot via `--webapp_url`

> [!NOTE]
> Free ngrok URLs are temporary and change each session. You'll need to re‑run the setup if the Colab runtime restarts.

---

## 🔐 Owner-Only: Update Bot Token

The notebook includes a **Token Encrypt/Decrypt Tool** cell at the bottom. This is for the bot owner only.

**To update the bot token:**

1. Expand the `🔐 Owner-Only: Encrypt / Decrypt Bot Token` cell
2. Enter your **Owner Key** (the secret key set by the notebook author)
3. Choose **encrypt** as the action
4. Paste your raw bot token from [@BotFather](https://t.me/BotFather)
5. Run the cell — it outputs an encrypted string
6. Copy the encrypted string into the main cell's `_ENC_TOKEN` variable

> [!WARNING]
> Never share your raw bot token or owner key. The encryption is for basic obfuscation, not military-grade security.

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

All settings are Python variables at the top of the main cell. Expand it to edit.

| Variable | Default | Description |
|----------|---------|-------------|
| `ENABLE_DB` | `True` | Enable TiDB Cloud shared database (sticker data persists) |
| `ENABLE_WEBAPP` | `False` | Enable WebApp support via ngrok tunnel |
| `WEBAPP_PORT` | `8080` | Port for the internal WebApp server |
| `NGROK_AUTHTOKEN` | `""` | Your ngrok authtoken (required if WebApp enabled) |
| `DATA_DIR` | `"moe_sticker_bot_data"` | Directory where the bot stores data |
| `LOG_LEVEL` | `"info"` | Logging verbosity: `debug`, `info`, `warn`, or `error` |
| `HTTP_PROXY` | `""` | Optional HTTP proxy URL |
| `AUTO_RESTART` | `True` | Auto-restart bot on crash |
| `MAX_RESTARTS` | `5` | Maximum restart attempts before giving up |
| `KEEP_ALIVE` | `True` | Print heartbeat every 10 min to prevent Colab timeout |

---

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| **"Bot exited immediately"** | Check the STDERR output shown — it now displays the actual Go error. |
| **"insecure transport" DB error** | TiDB requires TLS. The notebook auto-patches this — just re-run. |
| **"Table doesn't exist"** | Database tables missing. Re-run — the bot auto-creates them on first connect. |
| **Bot stops after ~90 minutes** | This is normal on free Colab. Keep the tab active, or use Colab Pro. |
| **WebApp not working** | Set `ENABLE_WEBAPP = True` and provide a valid `NGROK_AUTHTOKEN`. |
| **ngrok URL not retrieved** | Check your ngrok auth token and ensure port `4040` isn't blocked. |
| **"Database disabled" warning** | This is fine — the bot works fully without a database. Set `ENABLE_DB = True` to connect. |
| **Build failed** | Check git clone / go build output. Try re-running the cell. |
| **Colors look wrong** | The notebook auto-detects light/dark mode. If colors are off, the terminal may not support OSC 11. |

For more detailed logs, set `LOG_LEVEL = "debug"` in the configuration variables.

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

This notebook is built upon the incredible work of **[Star-39](https://github.com/Star-39)** and all contributors to **[Moe-Sticker-Bot](https://github.com/star-39/moe-sticker-bot)**. Please show them some love!

### 📓 Colab Notebook Author

The Google Colab adaptation was crafted with ❤️ by **[Shinei Nouzen](https://github.com/Shineii86)**.  
If you find this notebook helpful, consider giving it a ⭐ and following for more Colab projects!

### 🛠️ Tools & Libraries

- [Moe-Sticker-Bot](https://github.com/star-39/moe-sticker-bot) — The core Telegram bot (Go)
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
