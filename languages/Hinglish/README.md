<h5 align="center">‎𐂐 Adapted from <a href="https://github.com/Star-39/Moe-Sticker-Bot">Star-39/Moe-Sticker-Bot</a></h5>

> [!IMPORTANT]
> • **Production ke liye Original Repository Use Karo**  
> • Ye Colab Notebook ek **Personal Customization** hai jo easy testing aur short‑term self‑hosting ke liye Google Colab mein design kiya gaya hai.  
> • 24/7 Deployments, Contributions, ya Full Feature Support (including WebApp) ke liye, please [Original Moe-Sticker-Bot Repository](https://github.com/Star-39/Moe-Sticker-Bot) ko refer karo.

<div align="center">

<sub>[English](https://github.com/Shineii86/MoeStickerBot/blob/main/README.md) • [中文（简体汉字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Simplified%20Han)/README.md) • [中文（繁體漢字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Traditional%20Han)/README.md) • [한국인](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Korean/README.md) • [Русский](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Russian/README.md) • [Hinglish](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Hinglish/README.md)</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go Version](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![Original Repo](https://img.shields.io/badge/Original-Star--39%2FMoe--Sticker--Bot-181717?style=flat&logo=github)](https://github.com/Star-39/Moe-Sticker-Bot)

[![GitHub Stars](https://img.shields.io/github/stars/Star-39/Moe-Sticker-Bot?style=for-the-badge&color=FFB6C1)](https://github.com/Star-39/Moe-Sticker-Bot/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Star-39/Moe-Sticker-Bot?style=for-the-badge&color=FF6B9D)](https://github.com/Star-39/Moe-Sticker-Bot/fork)

**LINE aur Kakao stickers ko Telegram mein import karo · Custom sticker sets banao · WebApp se sab kuch manage karo — sab kuch Google Colab mein free mein chal raha hai.**

</div>

---

<div align="center">

### 📢 Mere Telegram Sticker Channel ko Subscribe Karo!


<p align="center">
  <a href="https://t.me/MaximXStickers">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=dark">
      <source media="(prefers-color-scheme: light)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=light">
      <img src="https://telegramcard.vercel.app/?username=MaximXStickers&bgColor=rgba%28127%2C+29%2C+29%2C+1%29&textColor=%23fef2f2&subtleTextColor=%23fca5a5&extraColor=%23fbbf24&shadowColor=rgba%28251%2C+191%2C+36%2C+0.3%29&fontFamily=Arial%2C+sans-serif" alt="MaximXStickers Telegram Channel" width="850" />
    </picture>
  </a>
</p>

<i><p>Roz naye sticker packs, updates, aur exclusive content pao!</p></i>

</div>
<br>

---

## 📖 Table of Contents

- [🎯 Overview](#-overview)
- [📓 Apna Version Chuno](#-apna-version-chuno)
  - [v1 — Clean & Minimal](#v1--clean--minimal)
  - [v2 — Animated Colors](#v2--animated-colors)
  - [v3 — Terminal UI](#3--terminal--ui)
- [✨ Features](#-features)
- [🛠️ Prerequisites](#️-prerequisites)
  - [🔐 Telegram Bot Token Banao](#-telegram-bot-token-banao)
- [🚀 Quick Start](#-quick-start)
- [📚 Detailed Setup](#-detailed-setup)
  - [Step 1: Colab mein Open Karo](#step-1-colab-mein-open-karo)
  - [Step 2: Dependencies Install & Build](#step-2-dependencies-install--build)
  - [Step 3: Helper Scripts Download Karo](#step-3-helper-scripts-download-karo)
  - [Step 4: Configure & Launch](#step-4-configure--launch)
- [🌐 Optional: WebApp Enable Karo (ngrok)](#-optional-webapp-enable-karo-ngrok)
- [🤖 Bot Commands](#-bot-commands)
- [⚙️ Configuration Reference](#️-configuration-reference)
- [🔧 Troubleshooting](#-troubleshooting)
- [❓ FAQ](#-faq)
- [📄 License & Disclaimer](#-license--disclaimer)
- [💕 Credits & Acknowledgments](#-credits--acknowledgments)

---

## 🎯 Overview

**Moe Sticker Bot** ek powerful Telegram bot hai jo Go mein likha gaya hai aur aapko ye sab karne deta hai:

- 📥 LINE aur KakaoTalk sticker packs ko seedha Telegram mein **Import** karo
- 🎨 Kisi bhi image ya video se apne khud ke sticker sets **Create** karo
- 🛠️ Ek sundar drag‑and‑drop WebApp ke saath stickers ko **Manage** karo *(optional)*
- 💾 Telegram stickers ko multiple formats (PNG, WebP, GIF, WEBM) mein **Download** karo

Yeh **Google Colab Edition** poori setup ko ek hi notebook mein pack kar deta hai. Ye saari dependencies install karta hai, source se bot ko compile karta hai, aur background mein launch kar deta hai — koi VPS ya Docker ki zaroorat nahi. Testing, personal use, ya bas stickers ke saath maze karne ke liye perfect hai.

> [!NOTE]
>  Free Colab sessions lagbhag ~90 minutes ki inactivity ke baad disconnect ho jaate hain. 24/7 hosting ke liye VPS ya official Docker image consider karo.

---

## 📓 Apna Version Chuno

Apni pasand ka notebook choose karo:

### v1 — Clean & Minimal

- 🟢 Simple, seedha-saadha output
- ⚡ Fast — koi animations nahi, sirf zaroori jaankari
- ✅ Un users ke liye perfect jinhe bas kaam chalana hai

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV1.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-Simple%20%26%20Minimal-4ECDC4?style=for-the-badge&logo=googlecolab" alt="Open v1 in Colab">
  </a>
</p>

### v2 — Animated Colors

- 🎨 Background highlights ke saath poori ANSI color support
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ Lambe steps ke dauran animated braille spinners
- 💬 Success/error/warning badges ke saath clean, modern output
- ✨ Style aur readability ka best balance

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV2.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-Animated%20Colors-FF6B9D?style=for-the-badge&logo=googlecolab" alt="Open v2 in Colab">
  </a>
</p>

### v3 — Terminal UI

- 🖥️ Poora Terminal/ssh interface
- 🎨 ANSI colors, backgrounds, aur ASCII banners
- 📟 Ekdum "H4CK3R" feel dene ke liye simulated shell commands
- ✨ Demos, padhane, ya show‑off ke liye perfect

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV3.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-Terminal%20UI-8B5CF6?style=for-the-badge&logo=googlecolab" alt="Open v3 in Colab">
  </a>
</p>

---

### 💡 Pro Tip: Colab Ko Zyada Der Tak Chalana

Google Colab lagbhag ~90 minutes ki inactivity ke baad disconnect ho jaata hai. Bina paise diye uptime maximize karne ke liye:

1. **Colab widget ko minimize karo** – Neeche left mein **< >** button dabao taaki code/output panel collapse ho jaaye. Session minimize hone par bhi active rehta hai.
2. **Browser tab ko khula rakho** – Use band mat karo; aap doosre tabs mein switch kar sakte ho.
3. **Kabhi‑kabhi interact karo** – Har 30‑45 minutes mein notebook ke andar scroll ya click karte raho.

> 24/7 operation ke liye, **Colab Pro** upgrade karne ka vichaar karo (lambi runtimes) ya free VPS (jaise Oracle Cloud Always Free) par deploy karo.

---

## ✨ Features

| Category | Feature | Description |
|----------|---------|-------------|
| 📥 **Import** | LINE Stickers | LINE se static, animated, emoji, aur message stickers import karo |
| | KakaoTalk Stickers | Kakao emoticons (including animated) import aur decrypt karo |
| 🎨 **Creation** | Custom Packs | Images/videos (koi bhi format) se apne sticker sets banao |
| | Animated Stickers | Videos ko Telegram‑compatible WebM stickers mein convert karo |
| | Mixed Formats | Ek hi set mein static aur animated stickers milao |
| 🛠️ **Management** | WebApp Interface | Drag‑and‑drop reorder, emoji edit, stickers add/remove karo *(optional)* |
| | Edit Titles | Existing sticker sets ke naam badlo |
| 💾 **Download** | Batch Export | Poori sticker sets ko ZIP archives ke roop mein download karo |
| | Format Conversion | Stickers ko PNG, WebP, GIF, ya original format mein convert karo |
| 🔍 **Search** | Database Search | Pehle import kiye gaye sticker packs dhundho |
| ⚡ **Performance** | Multi‑threaded | Fast processing ke liye goroutines aur worker pools |

---

## 🛠️ Prerequisites

Aapko sirf do cheezein chahiye:

1. **Ek Google Account** (Colab ke liye)
2. **Ek Telegram Bot Token** ([@BotFather](https://t.me/BotFather) se)

### 🔐 Telegram Bot Token Banao

1. Telegram kholo aur **@BotFather** ko search karo.
2. Command `/newbot` bhejo.
3. Bot ke liye ek **naam** chuno (e.g., `My Sticker Bot`).
4. Ek **username** chuno jo `bot` mein khatam ho (e.g., `my_sticker_bot`).
5. BotFather aapko ek token dega jaise:
   ```
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
   ```
6. **Is token ko copy karo** — aapko Configuration step mein iski zaroorat hogi.

> 🔒 **Apna token secret rakho!** Jiske paas bhi ye hai, woh aapke bot ko control kar sakta hai.

---

## 🚀 Quick Start

```bash
# 1. Upar diye gaye "Open in Colab" badge par click karo
# 2. Sabhi cells run karo (Runtime → Run all)
# 3. Configuration cell mein apna Bot Token paste karo
# 4. (Optional) WebApp enable karo aur apna ngrok auth token daalo
# 5. Launch cell run karo
# 6. Telegram kholo aur apne bot ko /start bhejo
```

Bas itna hi! Notebook baaki sab kuch handle kar lega: Go install karna, system tools, Python helpers, aur bot compile karna.

---

## 📚 Detailed Setup

### Step 1: Colab mein Open Karo

Is README ke top par diye gaye **"Open in Colab"** badge par click karo. Ye notebook ko aapke Google Colab environment mein load kar dega.

### Step 2: Dependencies Install & Build

Pehla code cell sabhi zaroori system packages install karta hai aur bot ko compile karta hai.

**Kya install hota hai:**

```
System Packages:
├── imagemagick          → Image processing
├── ffmpeg               → Video/animation conversion
├── libarchive-tools     → Archive extraction (bsdtar)
├── curl, gifsicle       → Network & GIF tools
├── python3              → Helper scripts ke liye
└── exiv2                → Metadata handling

Go Compiler:
└── go1.21.5             → Go programming language

Build Output:
└── /content/Moe-Sticker-Bot/Moe-Sticker-Bot
```

**Expected output:**
```
✅ All system dependencies installed!
Go version: go1.21.5
exiv2 version: 0.27.3
ffmpeg version: 4.4.2
ImageMagick version: 6.9.11
```

### Step 3: Helper Scripts Download Karo

Doosra cell Python helper scripts download karta hai jo bot specialized tasks ke liye use karta hai:

| Script | Purpose |
|--------|---------|
| `msb_emoji.py` | Emoji representations extract aur assign karo |
| `msb_kakao_decrypt.py` | Animated KakaoTalk stickers ko decrypt karo |
| `msb_rlottie.py` | TGS (Telegram animated sticker) format convert karo |

Ye files `/usr/local/bin/` mein daali jaati hain taaki bot unhe dhundh sake.

### Step 4: Configure & Launch

Configuration cell mein woh saari settings hain jinhe aap adjust kar sakte ho. Kam se kam apna `BOT_TOKEN` enter karo. Configure karne ke baad **Launch** cell run karo.

---

## 🌐 Optional: WebApp Enable Karo (ngrok)

WebApp manager ko ek public HTTPS URL ki zaroorat hoti hai, jo Colab natively provide nahi karta. Notebook mein **ngrok** ke liye built‑in support hai jo ek secure tunnel create karta hai.

### Kaise Enable Karein

1. [ngrok.com](https://ngrok.com/) par **free ngrok account** ke liye sign up karo.
2. [Dashboard](https://dashboard.ngrok.com/auth) se apna **authtoken** copy karo.
3. **Configuration** cell mein:
   - `ENABLE_WEBAPP = True` set karo
   - `NGROK_AUTHTOKEN` mein token paste karo
   - (Optional) Zaroorat ho toh `WEBAPP_PORT` badal do
4. Sabhi cells run karo. Notebook automatically:
   - ngrok download aur install karega
   - WebApp port ke liye tunnel start karega
   - Public `https://` URL retrieve karega
   - `--webapp_url` ke through bot ko pass karega

> [!NOTE]
> Free ngrok URLs temporary hote hain aur har session badalte hain. Agar Colab runtime restart hota hai toh setup dobara karna padega.

---

## 🤖 Bot Commands

Ek baar running hone ke baad, Telegram par apne bot se in commands ke saath baat karo:

| Command | Description |
|---------|-------------|
| `/start` | Welcome message aur basic instructions |
| `/help` | Saare available commands dikhao |
| `/import` | Ek share link se LINE ya Kakao sticker pack import karo |
| `/search` | Pehle import kiye gaye sticker sets dhundho |
| `/create` | Apne images/videos se naya sticker set banao |
| `/manage` | Apne sticker sets ke liye WebApp manager kholo *(WebApp enabled hona chahiye)* |
| `/download` | Telegram stickers ya GIF download karo |
| `/crop` | Sticker banane se pehle image crop karo |
| `/resize` | Image ka size badlo |
| `/addtext` | Sticker par custom text daalo |
| `/emoji` | Emoji overlay add karo |
| `/convert` | WebM (animated) mein convert karo |
| `/delete` | Apna sticker set delete karo |

> 💡 **Tip**: Aap bot ko seedha **LINE/Kakao sticker link** bhi bhej sakte ho — woh automatically import karne ka offer dega.

---

## ⚙️ Configuration Reference

Notebook ye configuration options provide karta hai:

| Field | Required | Description |
|-------|----------|-------------|
| `BOT_TOKEN` | ✅ Haan | Aapka Telegram Bot Token |
| `ENABLE_DB` | ❌ Nahi | Shared sticker sets ke liye MariaDB enable karein |
| `DB_ADDR` / `DB_USER` / `DB_PASS` | Sirf agar DB enabled ho | Database connection details |
| `ENABLE_WEBAPP` | ❌ Nahi | ngrok ke through WebApp support enable karein |
| `WEBAPP_PORT` | Sirf agar WebApp ho | Internal WebApp server ke liye port (default: 8080) |
| `NGROK_AUTHTOKEN` | Sirf agar WebApp ho | Aapka free ngrok authtoken |
| `DATA_DIR` | ❌ Nahi | Bot data kahan store karega |
| `LOG_LEVEL` | ❌ Nahi | `debug`, `info`, `warn`, ya `error` |
| `HTTP_PROXY` | ❌ Nahi | Agar zaroorat ho toh proxy URL |

---

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| **"Bot exited immediately"** | `bot_stderr.log` check karo. Common reason: invalid token format. |
| **Missing exiv2 warning** | Dependency cell dobara run karo: `!apt-get install -y exiv2` |
| **Bot ~90 mins baad band ho jaata hai** | Free Colab par ye normal hai. Tab active rakho ya Colab Pro use karo. |
| **WebApp kaam nahi kar raha** | Ensure `ENABLE_WEBAPP = True` aur valid `NGROK_AUTHTOKEN` diya hai. |
| **ngrok URL nahi mil raha** | Check karo ngrok auth token sahi hai aur port `4040` block nahi hai. |
| **"Database not enabled" warning** | Ye theek hai — bot bina database ke bhi poora kaam karta hai. |

Zyada detailed logs ke liye Configuration cell mein `LOG_LEVEL = "debug"` set karo.

---

## ❓ FAQ

### Q: Kya ye sach mein free hai?
> **A:** Haan! Google Colab free hai, ngrok free tier deta hai, aur bot open‑source hai.

### Q: Kya main ise 24/7 chala sakta hoon?
> **A:** Free Colab sessions inactivity par disconnect ho jaate hain. Permanent hosting ke liye VPS ya official Docker image use karo.

### Q: Kya mujhe WebApp ki zaroorat hai?
> **A:** Nahi, ye completely optional hai. Bot iske bina bhi perfectly kaam karta hai; sirf drag‑and‑drop sticker management feature ke liye WebApp chahiye.

### Q: Kya main apne custom stickers use kar sakta hoon?
> **A:** Bilkul! Bot ko koi bhi image ya video bhejo, aur woh cropping, resizing, aur converting mein guide karega.

### Q: Kya animated stickers support hain?
> **A:** Haan! Bot videos ko WebM format mein convert karta hai aur ek hi pack mein static aur animated stickers dono support karta hai.

---

## 📄 License & Disclaimer

Yeh Colab notebook **Moe-Sticker-Bot** ke liye ek convenience wrapper hai, jo **GNU General Public License v3.0 (GPL‑3.0)** ke under licensed hai.

> [!WARNING]
> **Disclaimer**: Yeh notebook aapka personal Telegram Bot Token aur (optional) ngrok auth token use karta hai. Unhe secure rakhne ki zimmedari aapki hai. Authors kisi bhi misuse ya accidental exposure ke liye zimmedar nahi hain.

---

## 💕 Credits & Acknowledgments

### 🌟 Original Project

Yeh notebook **[Star-39](https://github.com/Star-39)** aur **[Moe-Sticker-Bot](https://github.com/Star-39/Moe-Sticker-Bot)** ke sabhi contributors ke shaandar kaam par based hai. Unhe thoda pyaar do!

### 📓 Colab Notebook Author

Google Colab adaptation **[Shinei Nouzen](https://github.com/Shineii86)** ne ❤️ ke saath banaya hai.  
Agar ye notebook helpful laga, toh ⭐ dena aur aur Colab projects ke liye follow karna mat bhoolna!

### 🛠️ Tools & Libraries

- [Moe-Sticker-Bot](https://github.com/Star-39/Moe-Sticker-Bot) — Core Telegram bot (Go)
- [ImageMagick](https://imagemagick.org/) — Image processing
- [ffmpeg](https://ffmpeg.org/) — Video conversion
- [exiv2](https://exiv2.org/) — Metadata handling
- [ngrok](https://ngrok.com/) — WebApp ke liye secure tunnel
- [Google Colab](https://colab.research.google.com/) — Free cloud runtime
- [tqdm](https://github.com/tqdm/tqdm) — Progress bars

---

<div align="center">

### 💕 Projects Ko Support Karo

⭐ **[Star-39/Moe-Sticker-Bot ko star do](https://github.com/Star-39/Moe-Sticker-Bot)**  
⭐ **[Is Colab notebook ko star do](https://github.com/Shineii86/MoeStickerBot)**

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
