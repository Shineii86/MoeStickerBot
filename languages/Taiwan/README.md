<h5 align="center">‎𐂐 改編自 <a href="https://github.com/Shineii86/MoeStickersBot">Shineii86/MoeStickersBot</a></h5>

> [!IMPORTANT]
> • **正式部署請使用原始儲存庫**  
> • 此 Colab 筆記本為**個人化訂製版**，目的在於讓使用者能在 Google Colab 中輕鬆測試與短期自託管。  
> • 若需要 24/7 運作、貢獻程式碼或完整功能支援（包含 WebApp），請參考 [原始 MoeStickersBot 儲存庫](https://github.com/Shineii86/MoeStickersBot)。

<div align="center">

<sub>[English](https://github.com/Shineii86/MoeStickerBot/blob/main/README.md) • [繁體中文 (台灣)](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Taiwan/README.md) • [中文（简体汉字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Simplified%20Han)/README.md) • [中文（繁體漢字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Traditional%20Han)/README.md) • [한국인](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Korean/README.md) • [Русский](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Russian/README.md)</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go Version](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![原始儲存庫](https://img.shields.io/badge/Original-Star--39%2FMoe--Sticker--Bot-181717?style=flat&logo=github)](https://github.com/Shineii86/MoeStickersBot)

[![GitHub Stars](https://img.shields.io/github/stars/Shineii86/MoeStickersBot?style=for-the-badge&color=FFB6C1)](https://github.com/Shineii86/MoeStickersBot/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Shineii86/MoeStickersBot?style=for-the-badge&color=FF6B9D)](https://github.com/Shineii86/MoeStickersBot/fork)

**匯入 LINE 和 Kakao 貼圖到 Telegram · 建立自訂貼圖集 · 透過 WebApp 管理一切 — 全部免費在 Google Colab 上執行。**

</div>

---

<div align="center">

### 📢 訂閱我的 Telegram 貼圖頻道！


<p align="center">
  <a href="https://t.me/MaximXStickers">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=dark">
      <source media="(prefers-color-scheme: light)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=light">
      <img src="https://telegramcard.vercel.app/?username=MaximXStickers&bgColor=rgba%28127%2C+29%2C+29%2C+1%29&textColor=%23fef2f2&subtleTextColor=%23fca5a5&extraColor=%23fbbf24&shadowColor=rgba%28251%2C+191%2C+36%2C+0.3%29&fontFamily=Arial%2C+sans-serif" alt="MaximXStickers Telegram 頻道" width="850" />
    </picture>
  </a>
</p>

<i><p>每日取得貼圖包、更新與獨家內容！</p></i>

</div>
<br>

---

## 📖 目錄

- [🎯 概述](#-overview)
- [📓 選擇你的版本](#-choose-your-version)
  - [v1 — 簡潔極簡](#v1--clean--minimal)
  - [v2 — 動畫色彩](#v2--animated--colors)
  - [v3 — 終端機介面](#3--terminal--ui)
- [✨ 功能特色](#-features)
- [🛠️ 前置需求](#️-prerequisites)
  - [🔐 建立 Telegram 機器人 Token](#-create-a-telegram-bot-token)
- [🚀 快速開始](#-quick-start)
- [📚 詳細設定](#-detailed-setup)
  - [步驟 1：在 Colab 中開啟](#step-1-open-in-colab)
  - [步驟 2：安裝相依套件與建置](#step-2-install-dependencies--build)
  - [步驟 3：下載輔助腳本](#step-3-download-helper-scripts)
  - [步驟 4：設定與啟動](#step-4-configure--launch)
- [🌐 選用：啟用 WebApp（ngrok）](#-optional-enable-webapp-ngrok)
- [🤖 機器人指令](#-bot-commands)
- [⚙️ 設定參考](#️-configuration-reference)
- [🔧 疑難排解](#-troubleshooting)
- [❓ 常見問題](#-faq)
- [📄 授權與免責聲明](#-license--disclaimer)
- [💕 致謝與鳴謝](#-credits--acknowledgments)

---

## 🎯 概述

**Moe Sticker Bot** 是一個以 Go 語言編寫的強大 Telegram 機器人，讓你可以：

- 📥 **匯入** LINE 和 KakaoTalk 貼圖包直接到 Telegram
- 🎨 **建立** 自己的貼圖集，可從任何圖片或影片製作
- 🛠️ **管理** 貼圖，透過美觀的拖放 WebApp（選用）
- 💾 **下載** Telegram 貼圖為多種格式（PNG、WebP、GIF、WEBM）

這個 **Google Colab 版本** 將整個設定封裝在單一筆記本中。它會安裝所有相依套件、從原始碼編譯機器人，並在背景啟動——不需要 VPS 或 Docker。非常適合測試、個人使用，或單純享受貼圖樂趣。

> [!NOTE]
> 免費 Colab 工作階段會在閒置約 90 分鐘後中斷連線。若需要 24/7 託管，建議使用 VPS 或官方 Docker 映像檔。

---

## 📓 選擇你的版本

挑選符合你風格的筆記本：

### v1 — 簡潔極簡

- 🟢 簡單直接的輸出
- ⚡ 快速 —— 沒有動畫，只有必要資訊
- ✅ 適合只想讓它直接運作的使用者

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV1.ipynb">
    <img src="https://img.shields.io/badge/在%20Colab%20中開啟-簡潔極簡-4ECDC4?style=for-the-badge&logo=googlecolab" alt="在 Colab 中開啟 v1">
  </a>
</p>

### v2 — 動畫色彩

- 🎨 完整 ANSI 色彩支援與背景高亮
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ 在較長的步驟中顯示動畫點字旋轉圖示
- 💬 乾淨、現代化的輸出，附帶成功/錯誤/警告標記
- ✨ 風格與可讀性之間的最佳平衡

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV2.ipynb">
    <img src="https://img.shields.io/badge/在%20Colab%20中開啟-動畫色彩-FF6B9D?style=for-the-badge&logo=googlecolab" alt="在 Colab 中開啟 v2">
  </a>
</p>

### v3 — 終端機介面

- 🖥️ 完整終端機/ssh 風格
- 🎨 ANSI 色彩、背景與 ASCII 橫幅
- 📟 模擬 shell 命令，打造真正的「H4CK3R」氛圍
- ✨ 非常適合演示、教學或炫耀

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV3.ipynb">
    <img src="https://img.shields.io/badge/在%20Colab%20中開啟-終端機介面-8B5CF6?style=for-the-badge&logo=googlecolab" alt="在 Colab 中開啟 v3">
  </a>
</p>

---

### 💡 專家提示：讓 Colab 運作更久

Google Colab 會在閒置約 90 分鐘後中斷連線。若要最大化執行時間而不付費：

1. **最小化 Colab 小工具** – 點擊左下角的 **< >** 按鈕來收合程式碼/輸出面板。工作階段在最小化時仍會保持活躍。
2. **保持瀏覽器分頁開啟** – 不要關閉分頁；你可以切換到其他分頁。
3. **偶爾互動** – 每 30～45 分鐘滾動或點擊筆記本內部。

> 若要 24/7 運作，可考慮升級到 **Colab Pro**（更長的執行時間）或部署在免費 VPS 上（例如 Oracle Cloud Always Free）。

---

## ✨ 功能特色

| 類別 | 功能 | 說明 |
|----------|---------|-------------|
| 📥 **匯入** | LINE 貼圖 | 匯入靜態、動態、表情及訊息貼圖 |
| | KakaoTalk 貼圖 | 匯入並解密 Kakao 表情貼（包含動畫貼圖） |
| 🎨 **創作** | 自訂貼圖包 | 從圖片/影片建立你自己的貼圖集（任何格式） |
| | 動畫貼圖 | 將影片轉換為 Telegram 相容的 WebM 貼圖 |
| | 混合格式 | 在同一個貼圖集中混合靜態與動畫貼圖 |
| 🛠️ **管理** | WebApp 介面 | 拖放排序、編輯表情符號、新增/移除貼圖（選用） |
| | 編輯標題 | 重新命名現有的貼圖集 |
| 💾 **下載** | 批次匯出 | 以 ZIP 壓縮檔下載整個貼圖集 |
| | 格式轉換 | 將貼圖轉換為 PNG、WebP、GIF 或原始格式 |
| 🔍 **搜尋** | 資料庫搜尋 | 尋找先前匯入的貼圖包 |
| ⚡ **效能** | 多執行緒 | 使用 Goroutines 與工作池進行快速處理 |

---

## 🛠️ 前置需求

你只需要兩樣東西：

1. **一個 Google 帳號**（用於 Colab）
2. **一個 Telegram Bot Token**（從 [@BotFather](https://t.me/BotFather) 取得）

### 🔐 建立 Telegram 機器人 Token

1. 開啟 Telegram 並搜尋 **@BotFather**。
2. 傳送指令 `/newbot`。
3. 為你的機器人選擇一個**名稱**（例如 `我的貼圖機器人`）。
4. 選擇一個以 `bot` 結尾的**使用者名稱**（例如 `my_sticker_bot`）。
5. BotFather 會回覆一個 Token，例如：
   ```
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
   ```
6. **複製這個 Token** —— 稍後設定步驟會用到。

> 🔒 **請妥善保管你的 Token！** 任何人拿到它就可以控制你的機器人。

---

## 🚀 快速開始

```bash
# 1. 點擊上方的「在 Colab 中開啟」標記
# 2. 執行所有儲存格（Runtime → Run all）
# 3. 在設定儲存格中貼上你的 Bot Token
# 4. （選用）啟用 WebApp 並加入你的 ngrok auth token
# 5. 執行啟動儲存格
# 6. 開啟 Telegram 傳送 /start 給你的機器人
```

這樣就完成了！筆記本會處理其餘所有事情：安裝 Go、系統工具、Python 輔助程式以及編譯機器人。

---

## 📚 詳細設定

### 步驟 1：在 Colab 中開啟

點擊本 README 頂端的 **「在 Colab 中開啟」** 標記，這會將筆記本載入你的 Google Colab 環境。

### 步驟 2：安裝相依套件與建置

第一個程式碼儲存格會安裝所有必要的系統套件並編譯機器人。

**會安裝什麼：**

```
系統套件：
├── imagemagick          → 圖片處理
├── ffmpeg               → 影片/動畫轉換
├── libarchive-tools     → 壓縮檔解壓 (bsdtar)
├── curl, gifsicle       → 網路與 GIF 工具
├── python3              → 供輔助腳本使用
└── exiv2                → 中繼資料處理

Go 編譯器：
└── go1.21.5             → Go 程式語言

建置輸出：
└── /content/MoeStickersBot/MoeStickersBot
```

**預期輸出：**
```
✅ 所有系統相依套件已安裝！
Go 版本： go1.21.5
exiv2 版本： 0.27.3
ffmpeg 版本： 4.4.2
ImageMagick 版本： 6.9.11
```

### 步驟 3：下載輔助腳本

第二個儲存格下載機器人用於特殊任務的 Python 輔助腳本：

| 腳本 | 用途 |
|--------|---------|
| `msb_emoji.py` | 擷取並指派表情符號 |
| `msb_kakao_decrypt.py` | 解密動態 KakaoTalk 貼圖 |
| `msb_rlottie.py` | 轉換 TGS（Telegram 動畫貼圖）格式 |

這些檔案會放到 `/usr/local/bin/`，以便機器人找到。

### 步驟 4：設定與啟動

設定儲存格包含所有可調整的選項。至少需要輸入 `BOT_TOKEN`。設定完成後，執行**啟動**儲存格。

---

## 🌐 選用：啟用 WebApp（ngrok）

WebApp 管理功能需要公開的 HTTPS 網址，Colab 原生並不提供。筆記本內建了對 **ngrok** 的支援，用以建立安全隧道。

### 如何啟用

1. **註冊免費 ngrok 帳號**：前往 [ngrok.com](https://ngrok.com/)。
2. 從[儀表板](https://dashboard.ngrok.com/auth)複製你的 **authtoken**。
3. 在**設定**儲存格中：
   - 將 `ENABLE_WEBAPP` 設為 `True`
   - 貼上你的 authtoken 至 `NGROK_AUTHTOKEN`
   - （可選）如有需要可變更 `WEBAPP_PORT`
4. 執行所有儲存格，筆記本將自動：
   - 下載並安裝 ngrok
   - 啟動通往 WebApp 連接埠的隧道
   - 取得公開的 `https://` 網址
   - 透過 `--webapp_url` 傳遞給機器人

> [!NOTE]
> 免費 ngrok 網址為暫時性網址，每次工作階段都會不同。若 Colab 執行環境重啟，需要重新執行設定。

---

## 🤖 機器人指令

當機器人運作後，你可以在 Telegram 中使用以下指令與之互動：

| 指令 | 描述 |
|---------|-------------|
| `/start` | 歡迎訊息與基本介紹 |
| `/help` | 顯示所有可用指令 |
| `/import` | 從分享連結匯入 LINE 或 Kakao 貼圖包 |
| `/search` | 搜尋先前匯入的貼圖集 |
| `/create` | 從你自己的圖片/影片建立新貼圖集 |
| `/manage` | 開啟貼圖集 WebApp 管理功能 *(需啟用 WebApp)* |
| `/download` | 下載 Telegram 貼圖或 GIF |
| `/crop` | 將圖片裁切後再製作成貼圖 |
| `/resize` | 調整圖片尺寸 |
| `/addtext` | 在貼圖上加上自訂文字 |
| `/emoji` | 加上表情符號覆疊 |
| `/convert` | 轉換為 WebM（動畫） |
| `/delete` | 刪除你擁有的貼圖集 |

> 💡 **提示**：你也可以直接傳送 **LINE/Kakao 貼圖連結**給機器人，它會自動詢問是否匯入。

---

## ⚙️ 設定參考

筆記本提供下列設定選項：

| 欄位 | 必填 | 描述 |
|-------|----------|-------------|
| `BOT_TOKEN` | ✅ 是 | 你的 Telegram Bot Token |
| `ENABLE_DB` | ❌ 否 | 啟用 MariaDB 以共用貼圖集 |
| `DB_ADDR` / `DB_USER` / `DB_PASS` | 僅啟用 DB 時 | 資料庫連線資訊 |
| `ENABLE_WEBAPP` | ❌ 否 | 透過 ngrok 啟用 WebApp 支援 |
| `WEBAPP_PORT` | 僅 WebApp 時 | 內部 WebApp 伺服器連接埠（預設：8080） |
| `NGROK_AUTHTOKEN` | 僅 WebApp 時 | 你的免費 ngrok authtoken |
| `DATA_DIR` | ❌ 否 | 機器人儲存資料的目錄 |
| `LOG_LEVEL` | ❌ 否 | `debug`、`info`、`warn` 或 `error` |
| `HTTP_PROXY` | ❌ 否 | 如有需要可設定代理伺服器 URL |

---

## 🔧 疑難排解

| 問題 | 解決方法 |
|-------|----------|
| **「機器人立即退出」** | 檢查 `bot_stderr.log`。常見原因：Token 格式無效。 |
| **缺少 exiv2 警告** | 重新執行相依套件儲存格：`!apt-get install -y exiv2` |
| **機器人約 90 分鐘後停止** | 這是免費 Colab 的正常現象。保持分頁活躍，或使用 Colab Pro。 |
| **WebApp 無法運作** | 確保 `ENABLE_WEBAPP = True` 且提供有效的 `NGROK_AUTHTOKEN`。 |
| **無法取得 ngrok 網址** | 檢查 ngrok auth token 是否正確，且連接埠 `4040` 未被阻擋。 |
| **「資料庫未啟用」警告** | 這是正常的 —— 機器人在沒有資料庫的情況下仍可完全運作。 |

如需更詳細的記錄，請在設定儲存格中將 `LOG_LEVEL` 設為 `"debug"`。

---

## ❓ 常見問題

### 問：這真的是免費的嗎？
> **答：** 是的！Google Colab 免費，ngrok 提供免費方案，且機器人是開源的。

### 問：我可以讓它 24/7 持續運作嗎？
> **答：** 免費 Colab 會在閒置後中斷連線。若要永久託管，建議使用 VPS 或官方 Docker 映像檔。

### 問：我需要 WebApp 嗎？
> **答：** 不需要，它完全是選用的。沒有它機器人也能完美運作；只有拖放式貼圖管理功能需要 WebApp。

### 問：我可以使用自己的自訂貼圖嗎？
> **答：** 當然可以！傳送任何圖片或影片給機器人，它會引導你進行裁切、調整大小與轉換。

### 問：它支援動畫貼圖嗎？
> **答：** 支援！機器人會將影片轉換成 WebM 格式，並支援在同一個貼圖包中混合靜態與動畫貼圖。

---

## 📄 授權與免責聲明

此 Colab 筆記本為 **MoeStickersBot** 的便捷封裝，該專案採用 **GNU General Public License v3.0 (GPL‑3.0)** 授權。

> [!WARNING]
> **免責聲明**：此筆記本會使用你的個人 Telegram Bot Token 以及（可選）ngrok auth token。你應自行負責保管它們的安全。作者對任何誤用或意外洩露不承擔任何責任。

---

## 💕 致謝與鳴謝

### 🌟 原始專案

此筆記本建立在 **[Star-39](https://github.com/Star-39)** 與所有貢獻者對 **[MoeStickersBot](https://github.com/Shineii86/MoeStickersBot)** 的驚人成果之上。請給予他們一些支持！

### 📓 Colab 筆記本作者

此 Google Colab 改編版本由 **[Shinei Nouzen](https://github.com/Shineii86)** 用心製作。  
如果你覺得這個筆記本有幫助，請考慮給它一顆 ⭐ 並關注更多 Colab 專案！

### 🛠️ 工具與函式庫

- [MoeStickersBot](https://github.com/Shineii86/MoeStickersBot) — 核心 Telegram 機器人 (Go)
- [ImageMagick](https://imagemagick.org/) — 圖片處理
- [ffmpeg](https://ffmpeg.org/) — 影片轉換
- [exiv2](https://exiv2.org/) — 中繼資料處理
- [ngrok](https://ngrok.com/) — 用於 WebApp 的安全隧道
- [Google Colab](https://colab.research.google.com/) — 免費雲端執行環境
- [tqdm](https://github.com/tqdm/tqdm) — 進度條

---

<div align="center">

### 💕 支持這些專案

⭐ **[給 Shineii86/MoeStickersBot 一顆星](https://github.com/Shineii86/MoeStickersBot)**  
⭐ **[給這個 Colab 筆記本一顆星](https://github.com/Shineii86/MoeStickerBot)**

<br>

<a href="https://github.com/Shineii86">
  <img src="https://img.shields.io/badge/Follow-@Shineii86-181717?style=for-the-badge&logo=github" alt="追蹤 Shineii86">
</a>
<a href="https://telegram.me/Shineii86">
  <img src="https://img.shields.io/badge/Telegram-@Shineii86-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram">
</a>

<img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=gradient&fontAlignY=30&section=footer">

<sup><b>原始機器人版權所有 © Star-39 及貢獻者。採用 GPL‑3.0 授權。<br>Colab 改編版 © Shinei Nouzen。保留所有權利。</b></sup>

</div>
