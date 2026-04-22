<h5 align="center">‎𐂐 改编自 <a href="https://github.com/Star-39/Moe-Sticker-Bot">Star-39/Moe-Sticker-Bot</a></h5>

> [!IMPORTANT]
> • **生产环境请使用原项目仓库**  
> • 此 Colab 笔记本为**个人定制版本**，旨在方便用户在 Google Colab 中进行快速测试和短期自托管。  
> • 如需 24/7 持续部署、贡献代码或使用完整功能（包括 WebApp），请参阅 [原版 Moe-Sticker-Bot 仓库](https://github.com/Star-39/Moe-Sticker-Bot)。

<div align="center">

<sub>[English](https://github.com/Shineii86/MoeStickerBot/blob/main/README.md) • [中文（简体汉字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Simplified%20Han)/README.md) • [中文（繁體漢字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Traditional%20Han)/README.md) • [한국인](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Korean/README.md) • [Русский](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Russian/README.md) • [Hinglish](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Hinglish/README.md)</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

[![许可证: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go 版本](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![原项目仓库](https://img.shields.io/badge/Original-Star--39%2FMoe--Sticker--Bot-181717?style=flat&logo=github)](https://github.com/Star-39/Moe-Sticker-Bot)

[![GitHub Stars](https://img.shields.io/github/stars/Star-39/Moe-Sticker-Bot?style=for-the-badge&color=FFB6C1)](https://github.com/Star-39/Moe-Sticker-Bot/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Star-39/Moe-Sticker-Bot?style=for-the-badge&color=FF6B9D)](https://github.com/Star-39/Moe-Sticker-Bot/fork)

**将 LINE 和 Kakao 贴纸导入 Telegram · 创建自定义贴纸包 · 通过 WebApp 管理一切 —— 全部在 Google Colab 上免费运行。**



</div>

---

<div align="center">

### 📢 订阅我的 Telegram 贴纸频道！


<p align="center">
  <a href="https://t.me/MaximXStickers">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=dark">
      <source media="(prefers-color-scheme: light)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=light">
      <img src="https://telegramcard.vercel.app/?username=MaximXStickers&bgColor=rgba%28127%2C+29%2C+29%2C+1%29&textColor=%23fef2f2&subtleTextColor=%23fca5a5&extraColor=%23fbbf24&shadowColor=rgba%28251%2C+191%2C+36%2C+0.3%29&fontFamily=Arial%2C+sans-serif" alt="MaximXStickers Telegram 频道" width="850" />
    </picture>
  </a>
</p>

<i><p>获取每日贴纸包、更新和独家内容！</p></i>

</div>
<br>

---

## 📖 目录

- [🎯 概述](#-概述)
- [📓 选择你的版本](#-选择你的版本)
  - [v1 — 简洁极简版](#v1--简洁极简版)
  - [v2 — 动态色彩版](#v2--动态色彩版)
  - [v3 — 终端 UI 版](#3--终端-ui-版)
- [✨ 功能特性](#-功能特性)
- [🛠️ 准备工作](#️-准备工作)
  - [🔐 创建 Telegram Bot 令牌](#-创建-telegram-bot-令牌)
- [🚀 快速开始](#-快速开始)
- [📚 详细设置](#-详细设置)
  - [步骤 1：在 Colab 中打开](#步骤-1在-colab-中打开)
  - [步骤 2：安装依赖并构建](#步骤-2安装依赖并构建)
  - [步骤 3：下载辅助脚本](#步骤-3下载辅助脚本)
  - [步骤 4：配置并启动](#步骤-4配置并启动)
- [🌐 可选：启用 WebApp (ngrok)](#-可选启用-webapp-ngrok)
- [🤖 机器人命令](#-机器人命令)
- [⚙️ 配置参考](#️-配置参考)
- [🔧 故障排除](#-故障排除)
- [❓ 常见问题](#-常见问题)
- [📄 许可证与免责声明](#-许可证与免责声明)
- [💕 致谢与鸣谢](#-致谢与鸣谢)

---

## 🎯 概述

**Moe Sticker Bot** 是一个用 Go 语言编写的强大 Telegram 机器人，可以让你：

- 📥 **导入** LINE 和 KakaoTalk 贴纸包直接到 Telegram
- 🎨 **创建** 来自任何图片或视频的自定义贴纸集
- 🛠️ **管理** 贴纸，通过精美的拖放式 WebApp *（可选）*
- 💾 **下载** Telegram 贴纸，支持多种格式（PNG、WebP、GIF、WEBM）

这个 **Google Colab 版本** 将整个设置打包到一个单独的笔记本中。它会安装所有依赖项，从源代码编译机器人，并在后台启动 —— 无需 VPS 或 Docker。非常适合测试、个人使用，或者纯粹为了玩贴纸找乐子。

> [!NOTE]
> 免费的 Colab 会话在不活动约 90 分钟后会断开连接。如果需要 24/7 托管，请考虑使用 VPS 或官方的 Docker 镜像。

---

## 📓 选择你的版本

挑选适合你风格的笔记本：

### v1 — 简洁极简版

- 🟢 输出简单、直接
- ⚡ 快速 —— 无动画，仅显示必要信息
- ✅ 非常适合只想让功能正常工作的用户

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV1.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-Simple%20%26%20Minimal-4ECDC4?style=for-the-badge&logo=googlecolab" alt="在 Colab 中打开 v1">
  </a>
</p>

### v2 — 动态色彩版

- 🎨 完整 ANSI 颜色支持，带背景高亮
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ 长时间步骤中显示动态盲文旋转动画
- 💬 干净、现代的输出，带有成功/错误/警告徽章
- ✨ 风格与可读性的最佳平衡

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV2.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-Animated%20Colors-FF6B9D?style=for-the-badge&logo=googlecolab" alt="在 Colab 中打开 v2">
  </a>
</p>

### v3 — 终端 UI 版

- 🖥️ 完整的终端/SSH 界面风格
- 🎨 ANSI 颜色、背景和 ASCII 横幅
- 📟 模拟 Shell 命令，带来真正的“黑客”氛围
- ✨ 非常适合演示、教学或炫耀

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV3.ipynb">
    <img src="https://img.shields.io/badge/Open%20in%20Colab-Terminal%20UI-8B5CF6?style=for-the-badge&logo=googlecolab" alt="在 Colab 中打开 v3">
  </a>
</p>

---

### 💡 专业提示：让 Colab 运行更久

Google Colab 在不活动约 90 分钟后会断开连接。想在不付费的情况下最大化运行时间：

1. **最小化 Colab 组件** – 点击左下角的 **< >** 按钮折叠代码/输出面板。会话在最小化状态下保持活跃。
2. **保持浏览器标签页打开** – 不要关闭它；你可以切换到其他标签页。
3. **偶尔互动** – 每 30-45 分钟在笔记本内滚动或点击一下。

> 如需 24/7 运行，可考虑升级到 **Colab Pro**（更长的运行时间）或部署在免费的 VPS 上（例如 Oracle Cloud 永久免费）。

---

## ✨ 功能特性

| 类别 | 功能 | 描述 |
|----------|---------|-------------|
| 📥 **导入** | LINE 贴纸 | 从 LINE 导入静态、动态、表情和消息贴纸 |
| | KakaoTalk 贴纸 | 导入并解密 Kakao 表情，包括动态表情 |
| 🎨 **创建** | 自定义贴纸包 | 从图片/视频（任意格式）构建你自己的贴纸集 |
| | 动态贴纸 | 将视频转换为 Telegram 兼容的 WebM 贴纸 |
| | 混合格式 | 在同一个贴纸集中组合静态和动态贴纸 |
| 🛠️ **管理** | WebApp 界面 | 拖放排序、编辑表情、添加/删除贴纸 *（可选）* |
| | 编辑标题 | 重命名现有的贴纸集 |
| 💾 **下载** | 批量导出 | 将整个贴纸集下载为 ZIP 压缩包 |
| | 格式转换 | 将贴纸转换为 PNG、WebP、GIF 或原始格式 |
| 🔍 **搜索** | 数据库搜索 | 查找之前导入的贴纸包 |
| ⚡ **性能** | 多线程 | 使用 Goroutine 和工作池进行快速处理 |

---

## 🛠️ 准备工作

你只需要两样东西：

1. **一个 Google 账号**（用于 Colab）
2. **一个 Telegram Bot 令牌**（从 [@BotFather](https://t.me/BotFather) 获取）

### 🔐 创建 Telegram Bot 令牌

1. 打开 Telegram 并搜索 **@BotFather**。
2. 发送命令 `/newbot`。
3. 为你的机器人选择一个**名称**（例如 `My Sticker Bot`）。
4. 选择一个以 `bot` 结尾的**用户名**（例如 `my_sticker_bot`）。
5. BotFather 会给你一个类似这样的令牌：
   ```
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
   ```
6. **复制此令牌** —— 稍后在配置步骤中会用到。

> 🔒 **请保密你的令牌！** 任何拥有它的人都可以控制你的机器人。

---

## 🚀 快速开始

```bash
# 1. 点击上方的 "在 Colab 中打开" 徽章
# 2. 运行所有单元格（运行时 → 全部运行）
# 3. 在“配置”单元格中，粘贴你的 Bot 令牌
# 4. （可选）启用 WebApp 并添加你的 ngrok 认证令牌
# 5. 运行“启动”单元格
# 6. 打开 Telegram 并向你的机器人发送 /start
```

就这样！笔记本会处理其余所有事情：安装 Go、系统工具、Python 辅助程序以及编译机器人。

---

## 📚 详细设置

### 步骤 1：在 Colab 中打开

点击此 README 顶部的 **“在 Colab 中打开”** 徽章。这会将笔记本加载到你的 Google Colab 环境中。

### 步骤 2：安装依赖并构建

第一个代码单元格会安装所有必需的系统软件包并编译机器人。

**将会安装的内容：**

```
系统软件包：
├── imagemagick          → 图像处理
├── ffmpeg               → 视频/动画转换
├── libarchive-tools     → 归档文件提取 (bsdtar)
├── curl, gifsicle       → 网络和 GIF 工具
├── python3              → 用于辅助脚本
└── exiv2                → 元数据处理

Go 编译器：
└── go1.21.5             → Go 编程语言

构建输出：
└── /content/Moe-Sticker-Bot/Moe-Sticker-Bot
```

**预期输出：**
```
✅ 所有系统依赖项已安装！
Go 版本： go1.21.5
exiv2 版本： 0.27.3
ffmpeg 版本： 4.4.2
ImageMagick 版本： 6.9.11
```

### 步骤 3：下载辅助脚本

第二个单元格会下载机器人用于特定任务的 Python 辅助脚本：

| 脚本 | 用途 |
|--------|---------|
| `msb_emoji.py` | 提取并分配表情符号表示 |
| `msb_kakao_decrypt.py` | 解密动态 KakaoTalk 贴纸 |
| `msb_rlottie.py` | 转换 TGS（Telegram 动态贴纸）格式 |

这些脚本会被放置在 `/usr/local/bin/` 中，以便机器人能够找到它们。

### 步骤 4：配置并启动

配置单元格包含所有你可以调整的设置。至少，你需要输入你的 `BOT_TOKEN`。配置完成后，运行**启动**单元格。

---

## 🌐 可选：启用 WebApp (ngrok)

WebApp 管理器需要一个公开的 HTTPS URL，而 Colab 本身不提供。笔记本内置了对 **ngrok** 的支持，用于创建一个安全的隧道。

### 如何启用

1. **在 [ngrok.com](https://ngrok.com/) 注册一个免费的 ngrok 账号**。
2. 从[仪表板](https://dashboard.ngrok.com/auth)复制你的 **authtoken**。
3. 在**配置**单元格中：
   - 设置 `ENABLE_WEBAPP = True`
   - 将你的令牌粘贴到 `NGROK_AUTHTOKEN`
   - （可选）如有需要，更改 `WEBAPP_PORT`
4. 运行所有单元格。笔记本会自动：
   - 下载并安装 ngrok
   - 启动指向 WebApp 端口的隧道
   - 获取公共的 `https://` URL
   - 通过 `--webapp_url` 参数传递给机器人

> [!NOTE]
> 免费的 ngrok URL 是临时的，并且每次会话都会更改。如果 Colab 运行时重启，你需要重新运行设置。

---

## 🤖 机器人命令

一旦运行，你可以使用以下命令在 Telegram 上与机器人交互：

| 命令 | 描述 |
|---------|-------------|
| `/start` | 欢迎信息和基本说明 |
| `/help` | 显示所有可用命令 |
| `/import` | 从分享链接导入 LINE 或 Kakao 贴纸包 |
| `/search` | 搜索之前导入的贴纸集 |
| `/create` | 从你自己的图片/视频创建新的贴纸集 |
| `/manage` | 打开贴纸集的 WebApp 管理器 *（需要启用 WebApp）* |
| `/download` | 下载 Telegram 贴纸或 GIF |
| `/crop` | 在制作贴纸前裁剪图片 |
| `/resize` | 调整图片尺寸 |
| `/addtext` | 为贴纸添加自定义文字 |
| `/emoji` | 添加表情符号覆盖层 |
| `/convert` | 转换为 WebM（动态）格式 |
| `/delete` | 删除你拥有的贴纸集 |

> 💡 **提示**：你也可以直接将 **LINE/Kakao 贴纸链接** 发送给机器人 —— 它会自动提供导入选项。

---

## ⚙️ 配置参考

笔记本提供以下配置选项：

| 字段 | 是否必填 | 描述 |
|-------|----------|-------------|
| `BOT_TOKEN` | ✅ 是 | 你的 Telegram Bot 令牌 |
| `ENABLE_DB` | ❌ 否 | 启用 MariaDB 用于共享贴纸集 |
| `DB_ADDR` / `DB_USER` / `DB_PASS` | 仅在启用 DB 时 | 数据库连接详情 |
| `ENABLE_WEBAPP` | ❌ 否 | 通过 ngrok 启用 WebApp 支持 |
| `WEBAPP_PORT` | 仅在启用 WebApp 时 | 内部 WebApp 服务器端口（默认：8080） |
| `NGROK_AUTHTOKEN` | 仅在启用 WebApp 时 | 你的免费 ngrok authtoken |
| `DATA_DIR` | ❌ 否 | 机器人存储数据的目录 |
| `LOG_LEVEL` | ❌ 否 | `debug`、`info`、`warn` 或 `error` |
| `HTTP_PROXY` | ❌ 否 | 需要的代理 URL |

---

## 🔧 故障排除

| 问题 | 解决方案 |
|-------|----------|
| **“机器人立即退出”** | 检查 `bot_stderr.log`。常见原因：令牌格式无效。 |
| **缺失 exiv2 警告** | 重新运行依赖项单元格：`!apt-get install -y exiv2` |
| **机器人在约 90 分钟后停止** | 这是免费 Colab 的正常现象。保持标签页活跃，或使用 Colab Pro。 |
| **WebApp 不工作** | 确保 `ENABLE_WEBAPP = True` 并且提供了有效的 `NGROK_AUTHTOKEN`。 |
| **无法获取 ngrok URL** | 检查你的 ngrok 认证令牌是否正确，以及端口 `4040` 是否未被阻止。 |
| **“数据库未启用”警告** | 这没关系 —— 机器人在没有数据库的情况下也能完全正常工作。 |

如需更详细的日志，请在配置单元格中将 `LOG_LEVEL = "debug"`。

---

## ❓ 常见问题

### 问：这真的是免费的吗？
> **答：** 是的！Google Colab 免费，ngrok 提供免费套餐，并且该机器人是开源的。

### 问：我可以让它 24/7 运行吗？
> **答：** 免费的 Colab 会话在不活动后会断开连接。如需永久托管，请考虑使用 VPS 或官方的 Docker 镜像。

### 问：我需要 WebApp 吗？
> **答：** 不需要，它是完全可选的。没有它，机器人也能完美运行；只有拖放式贴纸管理功能需要 WebApp。

### 问：我可以使用自己的自定义贴纸吗？
> **答：** 当然可以！向机器人发送任何图片或视频，它会指导你完成裁剪、调整大小和转换。

### 问：它支持动态贴纸吗？
> **答：** 是的！机器人将视频转换为 WebM 格式，并支持在同一贴纸包中混合静态和动态贴纸。

---

## 📄 许可证与免责声明

此 Colab 笔记本是 **Moe-Sticker-Bot** 的便捷封装版本，后者采用 **GNU General Public License v3.0 (GPL‑3.0)** 许可。

> [!WARNING]
> **免责声明**：此笔记本使用你个人的 Telegram Bot 令牌和（可选的）ngrok 认证令牌。你有责任确保其安全。作者不对任何误用或意外泄露承担责任。

---

## 💕 致谢与鸣谢

### 🌟 原项目

本笔记本基于 **[Star-39](https://github.com/Star-39)** 和 **[Moe-Sticker-Bot](https://github.com/Star-39/Moe-Sticker-Bot)** 所有贡献者的杰出工作构建。请为他们献上一些爱！

### 📓 Colab 笔记本作者

此 Google Colab 改编版由 **[Shinei Nouzen](https://github.com/Shineii86)** 倾心制作。  
如果你觉得这个笔记本有用，不妨给它一个 ⭐ 并关注我以获取更多 Colab 项目！

### 🛠️ 工具与库

- [Moe-Sticker-Bot](https://github.com/Star-39/Moe-Sticker-Bot) — 核心 Telegram 机器人（Go）
- [ImageMagick](https://imagemagick.org/) — 图像处理
- [ffmpeg](https://ffmpeg.org/) — 视频转换
- [exiv2](https://exiv2.org/) — 元数据处理
- [ngrok](https://ngrok.com/) — 用于 WebApp 的安全隧道
- [Google Colab](https://colab.research.google.com/) — 免费云端运行时
- [tqdm](https://github.com/tqdm/tqdm) — 进度条

---

<div align="center">

### 💕 支持项目

⭐ **[给 Star-39/Moe-Sticker-Bot 一颗星](https://github.com/Star-39/Moe-Sticker-Bot)**  
⭐ **[给这个 Colab 笔记本一颗星](https://github.com/Shineii86/MoeStickerBot)**

<br>

<a href="https://github.com/Shineii86">
  <img src="https://img.shields.io/badge/Follow-@Shineii86-181717?style=for-the-badge&logo=github" alt="关注 Shineii86">
</a>
<a href="https://telegram.me/Shineii86">
  <img src="https://img.shields.io/badge/Telegram-@Shineii86-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram">
</a>

<img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=gradient&fontAlignY=30&section=footer">

<sup><b>原机器人版权归 Star-39 及贡献者所有。GPL‑3.0 许可。<br>Colab 改编版 © Shinei Nouzen。保留所有权利。</b></sup>

</div>
