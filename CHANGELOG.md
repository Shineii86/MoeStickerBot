# 📋 Changelog

All notable changes to this project will be documented in this file.

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
