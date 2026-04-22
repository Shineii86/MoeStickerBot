<h5 align="center">‎𐂐 改編自 <a href="https://github.com/Star-39/Moe-Sticker-Bot">Star-39/Moe-Sticker-Bot</a></h5>

> [!IMPORTANT]
> • **生產環境請使用原始儲存庫**  
> • 此 Colab 筆記本為**個人客製化版本**，旨在方便於 Google Colab 中快速測試與短期自架。  
> • 如需 24/7 部署、貢獻程式碼或完整功能支援（包含 WebApp），請參閱 [原始 Moe-Sticker-Bot 儲存庫](https://github.com/Star-39/Moe-Sticker-Bot)。

<div align="center">

<sub>[English](https://github.com/Shineii86/MoeStickerBot/blob/main/README.md) • [中文（简体汉字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Simplified%20Han)/README.md) • [中文（繁體漢字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Traditional%20Han)/README.md) • [한국인](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Korean/README.md) • [Русский](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Russian/README.md) • [Hinglish](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Hinglish/README.md)</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

[![授權條款：GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go 版本](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![原始儲存庫](https://img.shields.io/badge/Original-Star--39%2FMoe--Sticker--Bot-181717?style=flat&logo=github)](https://github.com/Star-39/Moe-Sticker-Bot)

[![GitHub 星星](https://img.shields.io/github/stars/Star-39/Moe-Sticker-Bot?style=for-the-badge&color=FFB6C1)](https://github.com/Star-39/Moe-Sticker-Bot/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Star-39/Moe-Sticker-Bot?style=for-the-badge&color=FF6B9D)](https://github.com/Star-39/Moe-Sticker-Bot/fork)

**從 LINE 與 Kakao 匯入貼圖至 Telegram · 建立自訂貼圖包 · 透過 WebApp 管理一切 —— 全部在 Google Colab 上免費執行。**

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

<i><p>每日更新貼圖包、最新消息與獨家內容！</p></i>

</div>
<br>

---

## 📖 目錄

- [🎯 概述](#-概述)
- [📓 選擇你的版本](#-選擇你的版本)
  - [v1 — 乾淨極簡](#v1--乾淨極簡)
  - [v2 — 動態色彩](#v2--動態色彩)
  - [v3 — 終端機介面](#3--終端機介面)
- [✨ 功能特色](#-功能特色)
- [🛠️ 前置需求](#️-前置需求)
  - [🔐 建立 Telegram Bot Token](#-建立-telegram-bot-token)
- [🚀 快速開始](#-快速開始)
- [📚 詳細設定步驟](#-詳細設定步驟)
  - [步驟 1：在 Colab 中開啟](#步驟-1在-colab-中開啟)
  - [步驟 2：安裝依賴套件與編譯](#步驟-2安裝依賴套件與編譯)
  - [步驟 3：下載輔助腳本](#步驟-3下載輔助腳本)
  - [步驟 4：設定並啟動](#步驟-4設定並啟動)
- [🌐 選擇性功能：啟用 WebApp (ngrok)](#-選擇性功能啟用-webapp-ngrok)
- [🤖 Bot 指令](#-bot-指令)
- [⚙️ 設定參考](#️-設定參考)
- [🔧 疑難排解](#-疑難排解)
- [❓ 常見問題](#-常見問題)
- [📄 授權條款與免責聲明](#-授權條款與免責聲明)
- [💕 鳴謝與致謝](#-鳴謝與致謝)

---

## 🎯 概述

**Moe Sticker Bot** 是一款以 Go 語言編寫、功能強大的 Telegram 機器人，讓你能夠：

- 📥 **匯入** LINE 與 KakaoTalk 貼圖包至 Telegram
- 🎨 **建立** 你自己的貼圖組，來源可以是任何圖片或影片
- 🛠️ **管理** 貼圖，透過美觀的拖放式 WebApp 介面 *（選用功能）*
- 💾 **下載** Telegram 貼圖，支援多種格式（PNG、WebP、GIF、WEBM）

此 **Google Colab 版本** 將整個設定流程打包為單一筆記本。它會自動安裝所有依賴套件、從原始碼編譯機器人，並在背景啟動執行 —— 無需 VPS 或 Docker。非常適合測試、個人使用，或單純享受玩貼圖的樂趣。

> [!NOTE]
> 免費 Colab 工作階段會在閒置約 90 分鐘後中斷連線。如需 24/7 持續運作，請考慮使用 VPS 或官方 Docker 映像檔。

---

## 📓 選擇你的版本

挑選最符合你風格的筆記本：

### v1 — 乾淨極簡

- 🟢 輸出簡潔、直覺
- ⚡ 快速 —— 無動畫，僅顯示必要資訊
- ✅ 適合只想讓它「能用就好」的使用者

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV1.ipynb">
    <img src="https://img.shields.io/badge/在%20Colab%20開啟-簡潔極簡-4ECDC4?style=for-the-badge&logo=googlecolab" alt="在 Colab 開啟 v1">
  </a>
</p>

### v2 — 動態色彩

- 🎨 完整 ANSI 色彩支援，包含背景高亮
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ 長時間步驟使用動態點字旋轉動畫
- 💬 乾淨現代的輸出，附帶成功／錯誤／警告標誌
- ✨ 風格與可讀性的最佳平衡

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV2.ipynb">
    <img src="https://img.shields.io/badge/在%20Colab%20開啟-動態色彩-FF6B9D?style=for-the-badge&logo=googlecolab" alt="在 Colab 開啟 v2">
  </a>
</p>

### v3 — 終端機介面

- 🖥️ 完整的終端機／ssh 風格
- 🎨 ANSI 色彩、背景與 ASCII 橫幅標題
- 📟 模擬 Shell 指令，營造真實的「H4CK3R」氛圍
- ✨ 非常適合展示、教學或炫耀

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV3.ipynb">
    <img src="https://img.shields.io/badge/在%20Colab%20開啟-終端機介面-8B5CF6?style=for-the-badge&logo=googlecolab" alt="在 Colab 開啟 v3">
  </a>
</p>

---

### 💡 專業提示：讓 Colab 運行更久

Google Colab 在閒置約 90 分鐘後會中斷連線。若要在不付費的狀況下最大化運行時間：

1. **最小化 Colab 小工具** – 點擊左下角的 **< >** 按鈕以摺疊程式碼／輸出面板。最小化後工作階段仍會保持活躍。
2. **保持瀏覽器分頁開啟** – 不要關閉分頁；你可以切換到其他分頁。
3. **偶爾進行互動** – 每 30 至 45 分鐘在筆記本內捲動或點擊一下。

> 如需 24/7 持續運作，可考慮升級至 **Colab Pro**（更長的運行時間），或部署於免費 VPS（例如 Oracle Cloud Always Free）。

---

## ✨ 功能特色

| 類別 | 功能 | 說明 |
|----------|---------|-------------|
| 📥 **匯入** | LINE 貼圖 | 從 LINE 匯入靜態、動態、表情符號及訊息貼圖 |
| | KakaoTalk 貼圖 | 匯入並解密 Kakao 表情貼，包含動態貼圖 |
| 🎨 **創作** | 自訂貼圖包 | 從圖片／影片（任何格式）建立專屬貼圖組 |
| | 動態貼圖 | 將影片轉換為 Telegram 相容的 WebM 貼圖 |
| | 混合格式 | 在同一個貼圖組中結合靜態與動態貼圖 |
| 🛠️ **管理** | WebApp 介面 | 拖放排序、編輯表情符號、新增／移除貼圖 *（選用）* |
| | 編輯標題 | 重新命名現有的貼圖組 |
| 💾 **下載** | 批次匯出 | 將整個貼圖組下載為 ZIP 壓縮檔 |
| | 格式轉換 | 將貼圖轉換為 PNG、WebP、GIF 或原始格式 |
| 🔍 **搜尋** | 資料庫搜尋 | 尋找先前匯入過的貼圖包 |
| ⚡ **效能** | 多執行緒 | 使用 Goroutines 與工作池實現快速處理 |

---

## 🛠️ 前置需求

你只需要兩樣東西：

1. **一個 Google 帳戶**（用於 Colab）
2. **一個 Telegram Bot Token**（從 [@BotFather](https://t.me/BotFather) 取得）

### 🔐 建立 Telegram Bot Token

1. 開啟 Telegram，搜尋 **@BotFather**。
2. 傳送指令 `/newbot`。
3. 為你的機器人選擇一個**名稱**（例如 `我的貼圖機器人`）。
4. 選擇一個以 `bot` 結尾的**使用者名稱**（例如 `my_sticker_bot`）。
5. BotFather 會給你一組 Token，格式如下：
   ```
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
   ```
6. **複製此 Token** —— 稍後在設定步驟中會用到。

> 🔒 **請妥善保管你的 Token！** 任何持有此 Token 的人都可以控制你的機器人。

---

## 🚀 快速開始

```bash
# 1. 點擊上方的「在 Colab 開啟」徽章
# 2. 執行所有儲存格（執行階段 → 全部執行）
# 3. 在「設定」儲存格中，貼上你的 Bot Token
# 4. （選擇性）啟用 WebApp 並加入你的 ngrok auth token
# 5. 執行「啟動」儲存格
# 6. 開啟 Telegram，對你的機器人傳送 /start
```

這樣就完成了！筆記本會自動處理其餘所有事情：安裝 Go、系統工具、Python 輔助程式，以及編譯機器人。

---

## 📚 詳細設定步驟

### 步驟 1：在 Colab 中開啟

點擊本 README 頂部的 **「在 Colab 開啟」** 徽章。這會將筆記本載入你的 Google Colab 環境。

### 步驟 2：安裝依賴套件與編譯

第一個程式碼儲存格會安裝所有必要的系統套件並編譯機器人。

**將會安裝的內容：**

```
系統套件：
├── imagemagick          → 圖片處理
├── ffmpeg               → 影片／動畫轉換
├── libarchive-tools     → 壓縮檔解壓縮 (bsdtar)
├── curl, gifsicle       → 網路工具與 GIF 工具
├── python3              → 供輔助腳本使用
└── exiv2                → 中繼資料處理

Go 編譯器：
└── go1.21.5             → Go 程式語言

編譯輸出：
└── /content/Moe-Sticker-Bot/Moe-Sticker-Bot
```

**預期輸出：**
```
✅ 所有系統依賴套件已安裝完成！
Go 版本：go1.21.5
exiv2 版本：0.27.3
ffmpeg 版本：4.4.2
ImageMagick 版本：6.9.11
```

### 步驟 3：下載輔助腳本

第二個儲存格會下載機器人用於特殊任務的 Python 輔助腳本：

| 腳本 | 用途 |
|--------|---------|
| `msb_emoji.py` | 提取並指定對應的表情符號 |
| `msb_kakao_decrypt.py` | 解密 KakaoTalk 動態貼圖 |
| `msb_rlottie.py` | 轉換 TGS（Telegram 動態貼圖）格式 |

這些腳本會被放置於 `/usr/local/bin/`，以便機器人找到它們。

### 步驟 4：設定並啟動

「設定」儲存格包含所有可調整的選項。最低限度，請輸入你的 `BOT_TOKEN`。設定完成後，執行 **「啟動」** 儲存格。

---

## 🌐 選擇性功能：啟用 WebApp (ngrok)

WebApp 管理器需要一個公開的 HTTPS 網址，而 Colab 本身並未提供。此筆記本內建了 **ngrok** 支援，可用於建立安全通道。

### 如何啟用

1. **註冊免費 ngrok 帳戶**：前往 [ngrok.com](https://ngrok.com/)。
2. 從[儀表板](https://dashboard.ngrok.com/auth)複製你的 **authtoken**。
3. 在 **「設定」** 儲存格中：
   - 將 `ENABLE_WEBAPP` 設為 `True`
   - 將你的 Token 貼至 `NGROK_AUTHTOKEN`
   - （選擇性）視需要更改 `WEBAPP_PORT`
4. 執行所有儲存格。筆記本會自動：
   - 下載並安裝 ngrok
   - 建立通往 WebApp 連接埠的通道
   - 取得公開的 `https://` 網址
   - 透過 `--webapp_url` 參數傳遞給機器人

> [!NOTE]
> 免費 ngrok 網址為暫時性，每次工作階段都會變更。若 Colab 執行環境重啟，你需要重新執行設定步驟。

---

## 🤖 Bot 指令

機器人啟動後，你可以在 Telegram 中使用以下指令與它互動：

| 指令 | 說明 |
|---------|-------------|
| `/start` | 歡迎訊息與基本操作說明 |
| `/help` | 顯示所有可用指令 |
| `/import` | 從分享連結匯入 LINE 或 Kakao 貼圖包 |
| `/search` | 搜尋先前匯入過的貼圖組 |
| `/create` | 使用你自己的圖片或影片建立新的貼圖組 |
| `/manage` | 開啟 WebApp 管理你的貼圖組 *（需啟用 WebApp）* |
| `/download` | 下載 Telegram 貼圖或 GIF |
| `/crop` | 裁切圖片後再製作成貼圖 |
| `/resize` | 調整圖片尺寸 |
| `/addtext` | 在貼圖上加入自訂文字 |
| `/emoji` | 加入表情符號覆蓋層 |
| `/convert` | 轉換為 WebM（動態貼圖） |
| `/delete` | 刪除你所擁有的貼圖組 |

> 💡 **提示**：你也可以直接將 **LINE／Kakao 貼圖連結**傳送給機器人 —— 它會自動詢問是否匯入。

---

## ⚙️ 設定參考

筆記本提供以下設定選項：

| 欄位 | 必填 | 說明 |
|-------|----------|-------------|
| `BOT_TOKEN` | ✅ 是 | 你的 Telegram Bot Token |
| `ENABLE_DB` | ❌ 否 | 啟用 MariaDB 用於共享貼圖組 |
| `DB_ADDR` / `DB_USER` / `DB_PASS` | 僅當啟用 DB 時 | 資料庫連線詳細資訊 |
| `ENABLE_WEBAPP` | ❌ 否 | 透過 ngrok 啟用 WebApp 支援 |
| `WEBAPP_PORT` | 僅當啟用 WebApp | 內部 WebApp 伺服器連接埠（預設：8080） |
| `NGROK_AUTHTOKEN` | 僅當啟用 WebApp | 你的免費 ngrok authtoken |
| `DATA_DIR` | ❌ 否 | 機器人儲存資料的位置 |
| `LOG_LEVEL` | ❌ 否 | `debug`、`info`、`warn` 或 `error` |
| `HTTP_PROXY` | ❌ 否 | 必要時的代理伺服器網址 |

---

## 🔧 疑難排解

| 問題 | 解決方案 |
|-------|----------|
| **「機器人立即退出」** | 檢查 `bot_stderr.log`。常見原因：Token 格式無效。 |
| **缺少 exiv2 警告** | 重新執行依賴套件儲存格：`!apt-get install -y exiv2` |
| **機器人約 90 分鐘後停止** | 這是免費 Colab 的正常現象。保持分頁活躍，或使用 Colab Pro。 |
| **WebApp 無法運作** | 確認 `ENABLE_WEBAPP = True` 且提供了有效的 `NGROK_AUTHTOKEN`。 |
| **無法取得 ngrok 網址** | 確認 ngrok auth token 正確無誤，且連接埠 `4040` 未被阻擋。 |
| **「資料庫未啟用」警告** | 這是正常的 —— 即使沒有資料庫，機器人也能完整運作。 |

如需更詳細的記錄，可在「設定」儲存格中將 `LOG_LEVEL` 設為 `"debug"`。

---

## ❓ 常見問題

### Q：這真的免費嗎？
> **A：** 是的！Google Colab 是免費的，ngrok 提供免費方案，而機器人本身是開源軟體。

### Q：可以讓它 24/7 持續運行嗎？
> **A：** 免費 Colab 工作階段會在閒置後中斷。如需永久託管，請考慮使用 VPS 或官方 Docker 映像檔。

### Q：一定要使用 WebApp 嗎？
> **A：** 不需要，這完全是選用功能。即使沒有它，機器人也能完美運作；僅拖放式貼圖管理功能需要 WebApp。

### Q：可以使用我自己自訂的貼圖嗎？
> **A：** 當然可以！將任何圖片或影片傳送給機器人，它會引導你完成裁切、調整大小與轉換步驟。

### Q：支援動態貼圖嗎？
> **A：** 是的！機器人會將影片轉換為 WebM 格式，並支援在同一個貼圖包中混合靜態與動態貼圖。

---

## 📄 授權條款與免責聲明

此 Colab 筆記本是 **Moe-Sticker-Bot** 的便利封裝版本，後者採用 **GNU General Public License v3.0 (GPL‑3.0)** 授權。

> [!WARNING]
> **免責聲明**：此筆記本會使用你的個人 Telegram Bot Token 以及（選擇性）ngrok auth token。你有責任確保它們的安全。作者對於任何濫用或意外洩漏不承擔任何責任。

---

## 💕 鳴謝與致謝

### 🌟 原始專案

此筆記本奠基於 **[Star-39](https://github.com/Star-39)** 以及 **[Moe-Sticker-Bot](https://github.com/Star-39/Moe-Sticker-Bot)** 所有貢獻者的傑出成果。請給他們一些鼓勵！

### 📓 Colab 筆記本作者

Google Colab 改編版本由 **[Shinei Nouzen](https://github.com/Shineii86)** 用心打造。  
如果你覺得此筆記本實用，歡迎給它一顆 ⭐ 並關注以獲得更多 Colab 專案更新！

### 🛠️ 使用的工具與函式庫

- [Moe-Sticker-Bot](https://github.com/Star-39/Moe-Sticker-Bot) — 核心 Telegram 機器人（Go）
- [ImageMagick](https://imagemagick.org/) — 圖片處理
- [ffmpeg](https://ffmpeg.org/) — 影片轉換
- [exiv2](https://exiv2.org/) — 中繼資料處理
- [ngrok](https://ngrok.com/) — 用於 WebApp 的安全通道
- [Google Colab](https://colab.research.google.com/) — 免費雲端執行環境
- [tqdm](https://github.com/tqdm/tqdm) — 進度條顯示

---

<div align="center">

### 💕 支持這些專案

⭐ **[給 Star-39/Moe-Sticker-Bot 一顆星星](https://github.com/Star-39/Moe-Sticker-Bot)**  
⭐ **[給此 Colab 筆記本一顆星星](https://github.com/Shineii86/MoeStickerBot)**

<br>

<a href="https://github.com/Shineii86">
  <img src="https://img.shields.io/badge/追蹤-@Shineii86-181717?style=for-the-badge&logo=github" alt="追蹤 Shineii86">
</a>
<a href="https://telegram.me/Shineii86">
  <img src="https://img.shields.io/badge/Telegram-@Shineii86-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram">
</a>

<img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=gradient&fontAlignY=30&section=footer">

<sup><b>原始機器人版權所有 © Star-39 與貢獻者。採用 GPL‑3.0 授權。<br>Colab 改編版權所有 © Shinei Nouzen。保留所有權利。</b></sup>

</div>
