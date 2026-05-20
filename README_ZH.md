<h5 align="center">‎𐂐 改编自 <a href="https://github.com/Shineii86/MoeStickersBot">Shineii86/MoeStickesBot</a></h5>

> [!IMPORTANT]
> • **生产环境请使用原版仓库**  
> • 本 Colab 笔记本是**个人定制版**，专为在 Google Colab 中快速测试和短期自托管而设计。  
> • 如需 24/7 部署、贡献代码或使用完整功能（包括 WebApp），请参考原版 [Moe-Sticker-Bot](https://github.com/star-39/moe-sticker-bot) 仓库。

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go Version](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![Original Repo](https://img.shields.io/badge/Original-star-39%2Fmoe-sticker-bot-181717?style=flat&logo=github)](https://github.com/star-39/moe-sticker-bot)

[![GitHub Stars](https://img.shields.io/github/stars/Shineii86/MoeStickersBot?style=for-the-badge&color=FFB6C1)](https://github.com/Shineii86/MoeStickersBot/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Shineii86/MoeStickersBot?style=for-the-badge&color=FF6B9D)](https://github.com/Shineii86/MoeStickersBot/fork)

**导入 LINE 和 Kakao 贴纸到 Telegram · 创建自定义贴纸包 · 通过 WebApp 管理一切 — 全部在 Google Colab 中免费运行。**

[🇺🇸 English](README.md) | 🇨🇳 中文

</div>

---

<div align="center">

### 📢 订阅我的 Telegram 贴纸频道！


<p align="center">
  <a href="https://t.me/MaximXStickers">
    <img src="https://telegramcard.vercel.app/?username=MaximXStickers&bgColor=rgba%28127%2C+29%2C+29%2C+1%29&textColor=%23fef2f2&subtleTextColor=%23fca5a5&extraColor=%23fbbf24&shadowColor=rgba%28251%2C+191%2C+36%2C+0.3%29&fontFamily=Arial%2C+sans-serif" alt="MaximXStickers Telegram Channel" width="850" />
  </a>
</p>

<i><p>每日获取贴纸包、更新和独家内容！</p></i>

</div>
<br>

---

## 📖 目录

- [🎯 概述](#-概述)
- [📓 笔记本](#-笔记本)
- [✨ 功能特性](#-功能特性)
- [🛠️ 前置要求](#️-前置要求)
  - [🔐 创建 Telegram Bot Token](#-创建-telegram-bot-token)
- [🚀 快速开始](#-快速开始)
- [📚 工作原理](#-工作原理)
  - [⚙️ 配置与 Bot Token](#️-配置与-bot-token)
  - [📦 依赖安装与构建](#-依赖安装与构建)
  - [🚀 启动与自动重启](#-启动与自动重启)
- [🌐 可选：启用 WebApp (ngrok)](#-可选启用-webapp-ngrok)
- [🔐 仅限管理员：更新 Bot Token](#-仅限管理员更新-bot-token)
- [🤖 Bot 命令](#-bot-命令)
- [⚙️ 配置参考](#️-配置参考)
- [🔧 故障排除](#-故障排除)
- [❓ 常见问题](#-常见问题)
- [📄 许可证与免责声明](#-许可证与免责声明)
- [💕 致谢](#-致谢)

---

## 🎯 概述

**Moe Sticker Bot** 是一个用 Go 语言编写的强大 Telegram 机器人，它可以：

- 📥 **导入** LINE 和 KakaoTalk 贴纸包到 Telegram
- 🎨 **创建** 你自己的贴纸包（支持任意图片或视频）
- 🛠️ **管理** 贴纸，配有精美的拖拽式 WebApp *（可选）*
- 💾 **下载** Telegram 贴纸，支持多种格式（PNG、WebP、GIF、WEBM）

这个 **Google Colab 版本** 将整个设置过程封装在一个笔记本中。它会安装所有依赖、从源码编译机器人并在后台启动 — 无需 VPS 或 Docker。非常适合测试、个人使用，或者就是想玩玩贴纸。

> [!NOTE]
> 免费 Colab 会话在约 90 分钟不活动后会断开连接。如需 24/7 托管，请考虑使用 VPS 或官方 Docker 镜像。

> [!WARNING]
> ⚠️ **中国大陆用户请注意**：Google Colab 在中国大陆无法直接访问（被 GFW 屏蔽）。你需要使用 VPN/代理才能访问。如果没有 VPN，可以考虑以下替代方案：
> - **[Kaggle Kernels](https://www.kaggle.com/code)** — 免费 GPU，无需 VPN，支持 Jupyter Notebook
> - **[百度 AI Studio](https://aistudio.baidu.com/)** — 国内免费 GPU 平台
> - **[阿里云 PAI-DSW](https://pai.console.aliyun.com/)** — 阿里云免费 GPU 实例
> - **自建 VPS** — 阿里云、腾讯云等国内云服务器

---

## 📓 笔记本

整个设置是一个**可折叠的代码单元格** — 代码默认隐藏，只需点击播放按钮即可。

- 🎨 完整的 ANSI 颜色支持，带背景高亮
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ 长时间操作时显示动画加载指示器
- 💬 简洁现代的输出，带成功/错误/警告标识
- 🔐 加密的 Bot Token — 无需手动输入
- 💓 保活心跳机制，防止 Colab 超时
- 🔄 崩溃时自动重启（最多 5 次）

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBot_ZH.ipynb">
    <img src="https://img.shields.io/badge/在%20Colab%20中打开-MoeStickerBot-FF6B9D?style=for-the-badge&logo=googlecolab" alt="在 Colab 中打开">
  </a>
</p>

---

### 💡 小技巧：让 Colab 运行更久

Google Colab 在约 90 分钟不活动后会断开连接。笔记本内置了**保活心跳机制**，每 10 分钟打印一次以防止超时。要最大化运行时间：

1. **保持浏览器标签页打开** — 不要关闭它；你可以切换到其他标签页。
2. **偶尔互动一下** — 每 30-45 分钟在笔记本中滚动或点击。
3. **心跳机制会处理剩下的事** — 每 10 分钟打印一次时间戳以保持会话活跃。

> 如需 24/7 运行，可以考虑升级到 **Colab Pro**（更长的运行时间）或部署在免费 VPS 上（如 Oracle Cloud Always Free）。

---

## ✨ 功能特性

| 类别 | 功能 | 描述 |
|------|------|------|
| 📥 **导入** | LINE 贴纸 | 从 LINE 导入静态、动态、表情和消息贴纸 |
| | KakaoTalk 贴纸 | 导入并解密 Kakao 表情包，包括动态贴纸 |
| 🎨 **创建** | 自定义贴纸包 | 从图片/视频构建你自己的贴纸包（任意格式） |
| | 动态贴纸 | 将视频转换为 Telegram 兼容的 WebM 贴纸 |
| | 混合格式 | 在同一个贴纸包中混合静态和动态贴纸 |
| 🛠️ **管理** | WebApp 界面 | 拖拽排序、编辑表情、添加/删除贴纸 *（可选）* |
| | 编辑标题 | 重命名已有的贴纸包 |
| 💾 **下载** | 批量导出 | 将整个贴纸包下载为 ZIP 压缩包 |
| | 格式转换 | 将贴纸转换为 PNG、WebP、GIF 或原始格式 |
| 🔍 **搜索** | 数据库搜索 | 查找之前导入的贴纸包 |
| ⚡ **性能** | 多线程 | 使用 Goroutine 和工作池实现快速处理 |

---

## 🛠️ 前置要求

你只需要两样东西：

1. **一个 Google 账号**（用于 Colab）
2. **一个 Telegram Bot Token**（从 [@BotFather](https://t.me/BotFather) 获取）

### 🔐 创建 Telegram Bot Token

1. 打开 Telegram 并搜索 **@BotFather**。
2. 发送命令 `/newbot`。
3. 为你的 bot 选择一个**名称**（例如 `My Sticker Bot`）。
4. 选择一个以 `bot` 结尾的**用户名**（例如 `my_sticker_bot`）。
5. BotFather 会给你一个类似这样的 token：
   ```
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
   ```
6. **复制这个 token** — 你将在配置步骤中用到它。

> 🔒 **保管好你的 token！** 任何拥有它的人都可以控制你的 bot。

---

## 🚀 快速开始

```bash
# 1. 点击上方的 "在 Colab 中打开" 徽章
# 2. 点击主单元格的 ▶ 播放按钮（代码是隐藏的 — 只显示标题）
# 3. 机器人使用预配置的加密 token，无需手动输入
# 4. （可选）在单元格内编辑 ENABLE_WEBAPP 和 NGROK_AUTHTOKEN
# 5. 打开 Telegram，向你的 bot 发送 /start
```

就这么简单！这个单元格处理一切：安装 Go、系统工具、Python 辅助脚本、编译机器人，以及带自动重启的启动。

---

## 📚 工作原理

整个 bot 设置都在**一个可折叠的单元格**中，标题为 `🚀 Moe Sticker Bot — Configuration & Launch`。在 Colab 中，代码默认隐藏 — 你只能看到标题和播放按钮。没有输入框，没有可编辑字段。

### ⚙️ 配置与 Bot Token

所有设置都定义在单元格顶部，作为 Python 变量：

```python
ENABLE_DB       = True        # TiDB Cloud 共享数据库
ENABLE_WEBAPP   = False       # 设为 True 通过 ngrok 暴露 WebApp
WEBAPP_PORT     = 8080
NGROK_AUTHTOKEN = ""          # ENABLE_WEBAPP=True 时必填
DATA_DIR        = "moe_sticker_bot_data"
LOG_LEVEL       = "info"      # debug, info, warn, error
HTTP_PROXY      = ""          # 可选的 http://proxy:port
AUTO_RESTART    = True        # 崩溃时自动重启
MAX_RESTARTS    = 5           # 最大重启次数
KEEP_ALIVE      = True        # 每 10 分钟发送心跳（防止 Colab 超时）
```

Bot Token 已**加密**并嵌入在单元格中。你不需要手动输入。如果需要更新它，请使用笔记本底部的**仅限管理员 Token 工具**单元格。

### 📦 依赖安装与构建

运行单元格时，它会自动：

1. **安装系统包** — `imagemagick`、`ffmpeg`、`libarchive-tools`、`curl`、`gifsicle`、`python3`、`exiv2`
2. **连接 TiDB Cloud** — 共享数据库，用于贴纸数据持久化
3. **下载 Go 1.22.4** — 从源码编译机器人
4. **获取 Python 辅助脚本** — `msb_emoji.py`、`msb_kakao_decrypt.py`、`msb_rlottie.py`
5. **克隆并构建** — 下载 bot 源码并编译优化后的二进制文件

### 🚀 启动与自动重启

构建完成后，单元格会：

- 验证 Bot Token 格式
- 可选启动 ngrok 隧道用于 WebApp
- 将 bot 作为子进程启动
- 实时流式输出带颜色的日志
- 崩溃时**自动重启**（最多 5 次）
- 每 10 分钟发送**保活心跳**以防止 Colab 超时

---

## 🌐 可选：启用 WebApp (ngrok)

WebApp 管理器需要一个公共 HTTPS URL，Colab 本身不提供。笔记本内置了对 **ngrok** 的支持，用于创建安全隧道。

### 如何启用

1. **注册免费 ngrok 账号**：[ngrok.com](https://ngrok.com/)。
2. 从[控制面板](https://dashboard.ngrok.com/auth)复制你的 **authtoken**。
3. **展开主单元格**（点击标题），然后编辑配置变量：
   - 设置 `ENABLE_WEBAPP = True`
   - 设置 `NGROK_AUTHTOKEN = "你的token"`
   - （可选）如需要可更改 `WEBAPP_PORT`
4. 运行单元格。它会自动：
   - 下载并安装 ngrok
   - 启动到 WebApp 端口的隧道
   - 获取公共 `https://` URL
   - 通过 `--webapp_url` 传递给 bot

> [!NOTE]
> 免费 ngrok URL 是临时的，每次会话都会变化。如果 Colab 运行时重启，你需要重新运行设置。

---

## 🔐 仅限管理员：更新 Bot Token

笔记本底部有一个 **Token 加密/解密工具**单元格。仅限 bot 管理员使用。

**更新 Bot Token 的步骤：**

1. 展开 `🔐 Owner-Only: Encrypt / Decrypt Bot Token` 单元格
2. 输入你的 **Owner Key**（笔记本作者设置的密钥）
3. 选择 **encrypt** 作为操作
4. 粘贴你从 [@BotFather](https://t.me/BotFather) 获取的原始 bot token
5. 运行单元格 — 它会输出一个加密字符串
6. 将加密字符串复制到主单元格的 `_ENC_TOKEN` 变量中

> [!WARNING]
> 永远不要分享你的原始 bot token 或 owner key。加密只是基本的混淆，不是军事级别的安全措施。

---

## 🤖 Bot 命令

运行后，在 Telegram 上使用以下命令与你的 bot 交互：

| 命令 | 描述 |
|------|------|
| `/start` | 欢迎消息和基本说明 |
| `/help` | 显示所有可用命令 |
| `/import` | 从分享链接导入 LINE 或 Kakao 贴纸包 |
| `/search` | 搜索之前导入的贴纸包 |
| `/create` | 从你自己的图片/视频创建新的贴纸包 |
| `/manage` | 打开 WebApp 管理器管理你的贴纸包 *（需要启用 WebApp）* |
| `/download` | 下载 Telegram 贴纸或 GIF |
| `/crop` | 在制作贴纸前裁剪图片 |
| `/resize` | 调整图片大小 |
| `/addtext` | 给贴纸添加自定义文字 |
| `/emoji` | 添加表情叠加 |
| `/convert` | 转换为 WebM（动态） |
| `/delete` | 删除你拥有的贴纸包 |

> 💡 **提示**：你也可以直接发送 **LINE/Kakao 贴纸链接**给 bot — 它会自动提示你导入。

---

## ⚙️ 配置参考

所有设置都是主单元格顶部的 Python 变量。展开单元格进行编辑。

| 变量 | 默认值 | 描述 |
|------|--------|------|
| `ENABLE_DB` | `True` | 启用 TiDB Cloud 共享数据库（贴纸数据持久化） |
| `ENABLE_WEBAPP` | `False` | 通过 ngrok 隧道启用 WebApp 支持 |
| `WEBAPP_PORT` | `8080` | 内部 WebApp 服务器端口 |
| `NGROK_AUTHTOKEN` | `""` | 你的 ngrok authtoken（启用 WebApp 时必填） |
| `DATA_DIR` | `"moe_sticker_bot_data"` | bot 存储数据的目录 |
| `LOG_LEVEL` | `"info"` | 日志详细级别：`debug`、`info`、`warn` 或 `error` |
| `HTTP_PROXY` | `""` | 可选的 HTTP 代理 URL |
| `AUTO_RESTART` | `True` | 崩溃时自动重启 bot |
| `MAX_RESTARTS` | `5` | 放弃前的最大重启尝试次数 |
| `KEEP_ALIVE` | `True` | 每 10 分钟打印心跳以防止 Colab 超时 |

---

## 🔧 故障排除

| 问题 | 解决方案 |
|------|----------|
| **"Bot exited immediately"** | 检查你的 token 是否有效。使用仅限管理员 Token 工具验证。 |
| **Bot 在约 90 分钟后停止** | 这在免费 Colab 上是正常的。保持标签页活跃，或使用 Colab Pro。 |
| **WebApp 不工作** | 设置 `ENABLE_WEBAPP = True` 并提供有效的 `NGROK_AUTHTOKEN`。 |
| **ngrok URL 未获取** | 检查你的 ngrok auth token，确保端口 `4040` 未被阻止。 |
| **"Database disabled" 警告** | 这没关系 — bot 完全可以在没有数据库的情况下工作。设置 `ENABLE_DB = True` 来连接。 |
| **构建失败** | 检查 git clone / go build 输出。尝试重新运行单元格。 |

如需更详细的日志，在配置变量中设置 `LOG_LEVEL = "debug"`。

---

## ❓ 常见问题

### Q: 这真的免费吗？
> **A:** 是的！Google Colab 是免费的，ngrok 提供免费套餐，而且 bot 是开源的。

### Q: 能 24/7 运行吗？
> **A:** 免费 Colab 会话在不活动后会断开连接。如需永久托管，请考虑 VPS 或官方 Docker 镜像。

### Q: 我需要 WebApp 吗？
> **A:** 不需要，它是完全可选的。Bot 没有它也能完美运行；只有拖拽式贴纸管理功能需要 WebApp。

### Q: 能用我自己的自定义贴纸吗？
> **A:** 当然可以！向 bot 发送任何图片或视频，它会引导你完成裁剪、调整大小和转换。

### Q: 支持动态贴纸吗？
> **A:** 支持！Bot 将视频转换为 WebM 格式，并支持在同一个贴纸包中同时包含静态和动态贴纸。

---

## 📄 许可证与免责声明

这个 Colab 笔记本是 **MoeStickersBot** 的便捷封装，后者基于 **GNU 通用公共许可证 v3.0 (GPL‑3.0)** 发布。

> [!WARNING]
> **免责声明**：这个笔记本使用你的个人 Telegram Bot Token 和（可选的）ngrok auth token。你有责任保管好它们。作者对任何误用或意外泄露不承担任何责任。

---

## 💕 致谢

### 🌟 原版项目

这个笔记本建立在 **[Star-39](https://github.com/Star-39)** 和所有 **[Moe-Sticker-Bot](https://github.com/star-39/moe-sticker-bot)** 贡献者的出色工作之上。请给他们一些支持！

### 📓 Colab 笔记本作者

Google Colab 改编版由 ❤️ **[Shinei Nouzen](https://github.com/Shineii86)** 制作。  
如果你觉得这个笔记本有帮助，考虑给个 ⭐ 并关注更多 Colab 项目！

### 🛠️ 工具与库

- [Moe-Sticker-Bot](https://github.com/star-39/moe-sticker-bot) — 核心 Telegram bot (Go)
- [ImageMagick](https://imagemagick.org/) — 图像处理
- [ffmpeg](https://ffmpeg.org/) — 视频转换
- [exiv2](https://exiv2.org/) — 元数据处理
- [ngrok](https://ngrok.com/) — WebApp 安全隧道
- [Google Colab](https://colab.research.google.com/) — 免费云运行时
- [tqdm](https://github.com/tqdm/tqdm) — 进度条

---

<div align="center">

### 💕 支持项目

⭐ **[给 Shineii86/MoeStickersBot 点个星](https://github.com/Shineii86/MoeStickersBot)**  
⭐ **[给这个 Colab 笔记本点个星](https://github.com/Shineii86/MoeStickerBot)**

<br>

<a href="https://github.com/Shineii86">
  <img src="https://img.shields.io/badge/Follow-@Shineii86-181717?style=for-the-badge&logo=github" alt="关注 Shineii86">
</a>
<a href="https://telegram.me/Shineii86">
  <img src="https://img.shields.io/badge/Telegram-@Shineii86-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram">
</a>

<img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=gradient&fontAlignY=30&section=footer">

<sup><b>原版 Bot 版权归 Star-39 及贡献者所有。GPL‑3.0 许可证。<br>Colab 改编版 © Shinei Nouzen。保留所有权利。</b></sup>

</div>
