# 📋 Changelog

All notable changes to this project will be documented in this file.

## [v1.4.5] — 2026-05-20

### Fixed
- Replaced misleading Colab alternatives with accurate options (VPN or self-hosted VPS/Docker)

## [v1.4.4] — 2026-05-20

### Added
- Added China accessibility note to Chinese README (Google Colab blocked by GFW)
- Listed alternative platforms: Kaggle Kernels, 百度 AI Studio, 阿里云 PAI-DSW

## [v1.4.3] — 2026-05-20

### Fixed
- Translated all user-facing output text in Chinese notebook to Chinese
- Banner, status messages, error messages, headers, and log labels all in Chinese

## [v1.4.2] — 2026-05-20

### Fixed
- Fixed Telegram channel card not rendering (replaced `<picture>` with `<img>` — GitHub doesn't support `<picture>`)
- Aligned Chinese README structure to exactly match English README
- Both READMEs now use identical markdown formatting

## [v1.4.1] — 2026-05-20

### Added
- Chinese Colab notebook as notebooks/MoeStickerBot_ZH.ipynb
- Chinese README now links to Chinese notebook

## [v1.4.0] — 2026-05-20

### Added
- Chinese (中文) README translation as README_ZH.md
- Language switcher links in both English and Chinese READMEs

## [v1.3.2] — 2026-05-20

### Fixed
- Removed T4 GPU requirement from notebook metadata (no GPU needed for this bot)

## [v1.3.1] — 2026-05-20

### Changed
- Replaced outdated "Choose Your Version" section with single "Notebook" section
- Updated Table of Contents to match

## [v1.3.0] — 2026-05-20

### Changed
- Updated README.md to match current single-cell notebook structure
- Replaced "Detailed Setup" with "How It Works" section (Configuration, Dependencies, Launch)
- Updated Configuration Reference table with all actual variables and defaults
- Added "Owner-Only: Update Bot Token" section explaining the token tool cell
- Updated Troubleshooting to match notebook's actual behavior
- Updated Pro Tip section to reflect keep-alive heartbeat feature

## [v1.2.0] — 2026-05-20

### Improved
- Added `#@title` to main code cell so code is collapsed by default in Colab
- Users see only the title and play button — no visible code, no input boxes
- Section title banners still present inside for readability when expanded

## [v1.1.0] — 2026-05-20

### Improved
- Added prominent section title banners to main notebook code cell for better readability
- Structured code into three clearly labeled phases: Setup & Build, Configure & Prepare, Launch
- Added descriptive sub-section headers with emoji indicators for each code block (Dependencies, Database, Go Language, Python Helpers, Build, ngrok, CLI, Log Colorizer, Cleanup, Keep-Alive)
- Added section titles to Owner-Only Token Tool cell (Imports, Encryption Core, Main Execution)
- Updated title banner from "ALL-IN-ONE CELL" to "Configuration & Launch" for clarity

## [v1.0.0] — 2026-05-20

### Added
- Initial Colab Edition notebook with all-in-one setup cell
- Encrypted bot token with owner-only decrypt/encrypt tool
- TiDB Cloud shared database integration
- Go language auto-download and build pipeline
- Python helper scripts (Emoji, Kakao Decrypt, Lottie)
- Auto-restart with configurable max attempts
- Keep-alive heartbeat thread for Colab timeout prevention
- ANSI color-coded terminal output with animated spinners
- Optional ngrok WebApp tunnel support
- Full README with setup instructions, FAQ, and troubleshooting
