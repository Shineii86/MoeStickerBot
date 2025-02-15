<h5 align="center">‎𐂐 <a href="https://github.com/Shineii86/MoeStickersBot">Shineii86/MoeStickersBot</a>에서 적용됨</h5>

> [!IMPORTANT]
> • **프로덕션 환경에서는 원본 저장소를 사용하십시오**  
> • 이 Colab 노트북은 Google Colab에서 간편한 테스트 및 단기 자체 호스팅을 위해 설계된 **개인 맞춤형 버전**입니다.  
> • 24시간 연중무휴 배포, 기여 또는 전체 기능 지원(WebApp 포함)이 필요한 경우 [원본 MoeStickersBot 저장소](https://github.com/Shineii86/MoeStickersBot)를 참조하십시오.

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=𝗠𝗼𝗲%20𝗦𝘁𝗶𝗰𝗸𝗲𝗿%20𝗕𝗼𝘁&fontAlignY=30&fontSize=100&desc=𝖢𝗈𝗅𝖺𝖻%20𝖤𝖽𝗂𝗍𝗂𝗈𝗇%20—%20𝖲𝖾𝗅𝖿‑𝖧𝗈𝗌𝗍%20𝖸𝗈𝗎𝗋%20𝖳𝖾𝗅𝖾𝗀𝗋𝖺𝗆%20𝖲𝗍𝗂𝖼𝗄𝖾𝗋%20𝖡𝗈𝗍&descSize=30" />

<sub>[English](https://github.com/Shineii86/MoeStickerBot/blob/main/README.md) • [中文（简体汉字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Simplified%20Han)/README.md) • [中文（繁體漢字）](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Chinese%20(Traditional%20Han)/README.md) • [한국인](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Korean/README.md) • [Русский](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Russian/README.md) • [Hinglish](https://github.com/Shineii86/MoeStickerBot/blob/main/languages/Hinglish/README.md)</sub>

[![라이선스: GPL v3](https://img.shields.io/badge/라이선스-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Go 버전](https://img.shields.io/badge/Go-1.21%2B-00ADD8?logo=go)](https://go.dev/)

[![원본 저장소](https://img.shields.io/badge/원본-Star--39%2FMoe--Sticker--Bot-181717?style=flat&logo=github)](https://github.com/Shineii86/MoeStickersBot)

[![GitHub 별](https://img.shields.io/github/stars/Shineii86/MoeStickersBot?style=for-the-badge&color=FFB6C1)](https://github.com/Shineii86/MoeStickersBot/stargazers)
[![GitHub 포크](https://img.shields.io/github/forks/Shineii86/MoeStickersBot?style=for-the-badge&color=FF6B9D)](https://github.com/Shineii86/MoeStickersBot/fork)

**LINE & 카카오 스티커를 Telegram으로 가져오기 · 나만의 스티커 세트 만들기 · WebApp으로 모든 것 관리 — Google Colab에서 무료로 실행.**

</div>

---

<div align="center">

### 📢 제 텔레그램 스티커 채널을 구독하세요!


<p align="center">
  <a href="https://t.me/MaximXStickers">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=dark">
      <source media="(prefers-color-scheme: light)" srcset="https://telegramcard.vercel.app/?username=MaximXStickers&theme=light">
      <img src="https://telegramcard.vercel.app/?username=MaximXStickers&bgColor=rgba%28127%2C+29%2C+29%2C+1%29&textColor=%23fef2f2&subtleTextColor=%23fca5a5&extraColor=%23fbbf24&shadowColor=rgba%28251%2C+191%2C+36%2C+0.3%29&fontFamily=Arial%2C+sans-serif" alt="MaximXStickers 텔레그램 채널" width="850" />
    </picture>
  </a>
</p>

<i><p>매일 새로운 스티커 팩, 업데이트 및 독점 콘텐츠를 받아보세요!</p></i>

</div>
<br>

---

## 📖 목차

- [🎯 개요](#-개요)
- [📓 버전 선택](#-버전-선택)
  - [v1 — 깔끔하고 미니멀](#v1--깔끔하고-미니멀)
  - [v2 — 애니메이션 색상](#v2--애니메이션-색상)
  - [v3 — 터미널 UI](#3--터미널-ui)
- [✨ 기능](#-기능)
- [🛠️ 사전 요구사항](#️-사전-요구사항)
  - [🔐 텔레그램 봇 토큰 생성](#-텔레그램-봇-토큰-생성)
- [🚀 빠른 시작](#-빠른-시작)
- [📚 상세 설정](#-상세-설정)
  - [1단계: Colab에서 열기](#1단계-colab에서-열기)
  - [2단계: 종속성 설치 및 빌드](#2단계-종속성-설치-및-빌드)
  - [3단계: 헬퍼 스크립트 다운로드](#3단계-헬퍼-스크립트-다운로드)
  - [4단계: 구성 및 실행](#4단계-구성-및-실행)
- [🌐 선택 사항: WebApp 활성화 (ngrok)](#-선택-사항-webapp-활성화-ngrok)
- [🤖 봇 명령어](#-봇-명령어)
- [⚙️ 구성 참조](#️-구성-참조)
- [🔧 문제 해결](#-문제-해결)
- [❓ 자주 묻는 질문](#-자주-묻는-질문)
- [📄 라이선스 및 면책 조항](#-라이선스-및-면책-조항)
- [💕 크레딧 및 감사 인사](#-크레딧-및-감사-인사)

---

## 🎯 개요

**Moe Sticker Bot**은 Go로 작성된 강력한 텔레그램 봇으로, 다음과 같은 작업을 할 수 있습니다:

- 📥 LINE 및 카카오톡 스티커 팩을 텔레그램으로 직접 **가져오기**
- 🎨 모든 이미지나 비디오로 나만의 스티커 세트 **만들기**
- 🛠️ 드래그 앤 드롭이 가능한 아름다운 WebApp으로 스티커 **관리하기** *(선택 사항)*
- 💾 텔레그램 스티커를 다양한 형식(PNG, WebP, GIF, WEBM)으로 **다운로드**

이 **Google Colab 에디션**은 전체 설정을 단일 노트북에 담았습니다. 모든 종속성을 설치하고, 소스에서 봇을 컴파일하며, 백그라운드에서 실행합니다 — VPS나 Docker가 필요 없습니다. 테스트, 개인 사용 또는 스티커로 즐기기에 완벽합니다.

> [!NOTE]
>  무료 Colab 세션은 약 90분 동안 활동이 없으면 연결이 끊어집니다. 24시간 호스팅을 원한다면 VPS나 공식 Docker 이미지를 고려하십시오.

---

## 📓 버전 선택

당신의 스타일에 맞는 노트북을 선택하세요:

### v1 — 깔끔하고 미니멀

- 🟢 단순하고 직관적인 출력
- ⚡ 빠름 — 애니메이션 없이 필수 정보만 표시
- ✅ 그냥 작동하기를 원하는 사용자에게 완벽

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV1.ipynb">
    <img src="https://img.shields.io/badge/Colab에서%20열기-단순%20%26%20미니멀-4ECDC4?style=for-the-badge&logo=googlecolab" alt="v1을 Colab에서 열기">
  </a>
</p>

### v2 — 애니메이션 색상

- 🎨 배경 강조가 있는 완전한 ANSI 색상 지원
- ⠋⠙⠹⠸⠼⠴⠦⠧⠇⠏ 긴 단계에서 애니메이션 점자 스피너
- 💬 성공/오류/경고 배지가 있는 깔끔하고 현대적인 출력
- ✨ 스타일과 가독성의 최적 균형

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV2.ipynb">
    <img src="https://img.shields.io/badge/Colab에서%20열기-애니메이션%20색상-FF6B9D?style=for-the-badge&logo=googlecolab" alt="v2를 Colab에서 열기">
  </a>
</p>

### v3 — 터미널 UI

- 🖥️ 완전한 터미널/ssh 인터페이스
- 🎨 ANSI 색상, 배경 및 ASCII 배너
- 📟 진정한 "H4CK3R" 느낌을 위한 시뮬레이션 셸 명령어
- ✨ 데모, 교육 또는 과시용으로 완벽

<p align="center">
  <a href="https://colab.research.google.com/github/Shineii86/MoeStickerBot/blob/main/notebooks/MoeStickerBotV3.ipynb">
    <img src="https://img.shields.io/badge/Colab에서%20열기-터미널%20UI-8B5CF6?style=for-the-badge&logo=googlecolab" alt="v3을 Colab에서 열기">
  </a>
</p>

---

### 💡 프로 팁: Colab을 더 오래 실행하기

Google Colab은 약 90분 동안 활동이 없으면 연결이 끊어집니다. 비용 없이 가동 시간을 최대화하려면:

1. **Colab 위젯 최소화** – 하단 왼쪽의 **< >** 버튼을 클릭하여 코드/출력 패널을 접습니다. 세션은 최소화된 상태에서도 활성 상태를 유지합니다.
2. **브라우저 탭을 열어 두기** – 닫지 마십시오; 다른 탭으로 전환해도 됩니다.
3. **가끔 상호 작용하기** – 30~45분마다 노트북 내에서 스크롤하거나 클릭하십시오.

> 24시간 작동을 원한다면 **Colab Pro**로 업그레이드(더 긴 런타임)하거나 무료 VPS(예: Oracle Cloud Always Free)에 배포하는 것을 고려하십시오.

---

## ✨ 기능

| 카테고리 | 기능 | 설명 |
|----------|---------|----------|
| 📥 **가져오기** | LINE 스티커 | LINE의 정적, 애니메이션, 이모지 및 메시지 스티커 가져오기 |
| | 카카오톡 스티커 | 애니메이션을 포함한 카카오 이모티콘 가져오기 및 복호화 |
| 🎨 **생성** | 사용자 정의 팩 | 이미지/비디오(모든 형식)로 나만의 스티커 세트 만들기 |
| | 애니메이션 스티커 | 비디오를 텔레그램 호환 WebM 스티커로 변환 |
| | 혼합 형식 | 하나의 세트에 정적 및 애니메이션 스티커 결합 |
| 🛠️ **관리** | WebApp 인터페이스 | 드래그 앤 드롭으로 순서 변경, 이모지 편집, 스티커 추가/제거 *(선택 사항)* |
| | 제목 편집 | 기존 스티커 세트 이름 변경 |
| 💾 **다운로드** | 일괄 내보내기 | 전체 스티커 세트를 ZIP 아카이브로 다운로드 |
| | 형식 변환 | 스티커를 PNG, WebP, GIF 또는 원본 형식으로 변환 |
| 🔍 **검색** | 데이터베이스 검색 | 이전에 가져온 스티커 팩 검색 |
| ⚡ **성능** | 멀티스레드 | 빠른 처리를 위한 고루틴 및 워커 풀 |

---

## 🛠️ 사전 요구사항

두 가지만 필요합니다:

1. **Google 계정** (Colab용)
2. **텔레그램 봇 토큰** ([@BotFather](https://t.me/BotFather)에서 발급)

### 🔐 텔레그램 봇 토큰 생성

1. 텔레그램을 열고 **@BotFather**를 검색합니다.
2. `/newbot` 명령어를 보냅니다.
3. 봇의 **이름**을 정합니다 (예: `내 스티커 봇`).
4. `bot`으로 끝나는 **사용자 이름**을 정합니다 (예: `my_sticker_bot`).
5. BotFather가 다음과 같은 토큰을 발급합니다:
   ```
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
   ```
6. **이 토큰을 복사**하십시오 — 설정 단계에서 필요합니다.

> 🔒 **토큰을 비밀로 유지하십시오!** 토큰을 가진 사람은 누구나 봇을 제어할 수 있습니다.

---

## 🚀 빠른 시작

```bash
# 1. 위의 "Colab에서 열기" 배지를 클릭합니다
# 2. 모든 셀을 실행합니다 (런타임 → 모두 실행)
# 3. 구성 셀에 봇 토큰을 붙여넣습니다
# 4. (선택 사항) WebApp을 활성화하고 ngrok 인증 토큰을 추가합니다
# 5. 실행 셀을 실행합니다
# 6. 텔레그램을 열고 봇에게 /start를 보냅니다
```

그게 전부입니다! 노트북이 Go, 시스템 도구, Python 헬퍼 및 봇 컴파일을 모두 처리합니다.

---

## 📚 상세 설정

### 1단계: Colab에서 열기

이 README 상단의 **"Colab에서 열기"** 배지를 클릭합니다. 그러면 노트북이 Google Colab 환경에 로드됩니다.

### 2단계: 종속성 설치 및 빌드

첫 번째 코드 셀은 필요한 모든 시스템 패키지를 설치하고 봇을 컴파일합니다.

**설치되는 항목:**

```
시스템 패키지:
├── imagemagick          → 이미지 처리
├── ffmpeg               → 비디오/애니메이션 변환
├── libarchive-tools     → 아카이브 추출 (bsdtar)
├── curl, gifsicle       → 네트워크 및 GIF 도구
├── python3              → 헬퍼 스크립트용
└── exiv2                → 메타데이터 처리

Go 컴파일러:
└── go1.21.5             → Go 프로그래밍 언어

빌드 출력:
└── /content/MoeStickersBot/MoeStickersBot
```

**예상 출력:**
```
✅ 모든 시스템 종속성이 설치되었습니다!
Go 버전: go1.21.5
exiv2 버전: 0.27.3
ffmpeg 버전: 4.4.2
ImageMagick 버전: 6.9.11
```

### 3단계: 헬퍼 스크립트 다운로드

두 번째 셀은 봇이 특수 작업에 사용하는 Python 헬퍼 스크립트를 다운로드합니다:

| 스크립트 | 목적 |
|--------|------------|
| `msb_emoji.py` | 이모지 표현 추출 및 할당 |
| `msb_kakao_decrypt.py` | 애니메이션 카카오톡 스티커 복호화 |
| `msb_rlottie.py` | TGS (텔레그램 애니메이션 스티커) 형식 변환 |

이 파일들은 봇이 찾을 수 있도록 `/usr/local/bin/`에 배치됩니다.

### 4단계: 구성 및 실행

구성 셀에는 조정할 수 있는 모든 설정이 포함되어 있습니다. 최소한 `BOT_TOKEN`을 입력하십시오. 구성 후 **실행** 셀을 실행합니다.

---

## 🌐 선택 사항: WebApp 활성화 (ngrok)

WebApp 관리자는 Colab에서 기본 제공되지 않는 공용 HTTPS URL이 필요합니다. 노트북에는 보안 터널 생성을 위한 **ngrok** 지원이 내장되어 있습니다.

### 활성화 방법

1. [ngrok.com](https://ngrok.com/)에서 **무료 ngrok 계정**에 가입합니다.
2. [대시보드](https://dashboard.ngrok.com/auth)에서 **authtoken**을 복사합니다.
3. **구성** 셀에서:
   - `ENABLE_WEBAPP = True`로 설정
   - `NGROK_AUTHTOKEN`에 토큰 붙여넣기
   - (선택 사항) 필요한 경우 `WEBAPP_PORT` 변경
4. 모든 셀을 실행합니다. 노트북이 자동으로:
   - ngrok 다운로드 및 설치
   - WebApp 포트로 터널 시작
   - 공용 `https://` URL 획득
   - `--webapp_url`을 통해 봇에 전달

> [!NOTE]
> 무료 ngrok URL은 임시적이며 세션마다 변경됩니다. Colab 런타임이 다시 시작되면 설정을 다시 실행해야 합니다.

---

## 🤖 봇 명령어

실행 중인 봇과 텔레그램에서 다음 명령어로 상호 작용하십시오:

| 명령어 | 설명 |
|---------|----------|
| `/start` | 환영 메시지 및 기본 지침 |
| `/help` | 사용 가능한 모든 명령어 표시 |
| `/import` | 공유 링크에서 LINE 또는 카카오 스티커 팩 가져오기 |
| `/search` | 이전에 가져온 스티커 세트 검색 |
| `/create` | 나만의 이미지/비디오로 새 스티커 세트 만들기 |
| `/manage` | 스티커 세트용 WebApp 관리자 열기 *(WebApp 필요)* |
| `/download` | 텔레그램 스티커 또는 GIF 다운로드 |
| `/crop` | 스티커로 만들기 전에 이미지 자르기 |
| `/resize` | 이미지 크기 조정 |
| `/addtext` | 스티커에 사용자 정의 텍스트 추가 |
| `/emoji` | 이모지 오버레이 추가 |
| `/convert` | WebM (애니메이션)으로 변환 |
| `/delete` | 소유한 스티커 세트 삭제 |

> 💡 **팁**: 봇에게 **LINE/카카오 스티커 링크**를 직접 보낼 수도 있습니다 — 그러면 자동으로 가져오기를 제안합니다.

---

## ⚙️ 구성 참조

노트북은 다음 구성 옵션을 제공합니다:

| 필드 | 필수 | 설명 |
|-------|----------|-------------|
| `BOT_TOKEN` | ✅ 예 | 텔레그램 봇 토큰 |
| `ENABLE_DB` | ❌ 아니요 | 공유 스티커 세트를 위해 MariaDB 활성화 |
| `DB_ADDR` / `DB_USER` / `DB_PASS` | DB 활성화 시만 | 데이터베이스 연결 세부 정보 |
| `ENABLE_WEBAPP` | ❌ 아니요 | ngrok을 통한 WebApp 지원 활성화 |
| `WEBAPP_PORT` | WebApp 활성화 시만 | 내부 WebApp 서버 포트 (기본값: 8080) |
| `NGROK_AUTHTOKEN` | WebApp 활성화 시만 | 무료 ngrok 인증 토큰 |
| `DATA_DIR` | ❌ 아니요 | 봇 데이터 저장 위치 |
| `LOG_LEVEL` | ❌ 아니요 | `debug`, `info`, `warn` 또는 `error` |
| `HTTP_PROXY` | ❌ 아니요 | 필요한 경우 프록시 URL |

---

## 🔧 문제 해결

| 문제 | 해결책 |
|----------|---------|
| **"봇이 즉시 종료됨"** | `bot_stderr.log` 확인. 일반적인 원인: 잘못된 토큰 형식. |
| **exiv2 누락 경고** | 종속성 셀 재실행: `!apt-get install -y exiv2` |
| **약 90분 후 봇 중지** | 무료 Colab의 정상적인 동작입니다. 탭을 활성 상태로 유지하거나 Colab Pro 사용. |
| **WebApp 작동 안 함** | `ENABLE_WEBAPP = True` 및 유효한 `NGROK_AUTHTOKEN` 설정 확인. |
| **ngrok URL 검색 실패** | ngrok 인증 토큰이 올바르고 포트 `4040`이 차단되지 않았는지 확인. |
| **"Database not enabled" 경고** | 정상입니다 — 봇은 데이터베이스 없이도 완벽하게 작동합니다. |

더 자세한 로그를 보려면 구성 셀에서 `LOG_LEVEL = "debug"`로 설정하십시오.

---

## ❓ 자주 묻는 질문

### Q: 정말 무료인가요?
> **A:** 네! Google Colab은 무료이며, ngrok도 무료 티어를 제공하고, 봇은 오픈 소스입니다.

### Q: 24시간 계속 실행할 수 있나요?
> **A:** 무료 Colab 세션은 비활성 시 연결이 끊어집니다. 영구 호스팅을 원한다면 VPS나 공식 Docker 이미지를 고려하십시오.

### Q: WebApp이 필요한가요?
> **A:** 아니요, 완전히 선택 사항입니다. 봇은 WebApp 없이도 완벽하게 작동합니다; 드래그 앤 드롭 스티커 관리 기능만 WebApp이 필요합니다.

### Q: 나만의 커스텀 스티커를 사용할 수 있나요?
> **A:** 물론입니다! 봇에게 이미지나 비디오를 보내면 자르기, 크기 조정, 변환 과정을 안내합니다.

### Q: 애니메이션 스티커를 지원하나요?
> **A:** 네! 봇은 비디오를 WebM 형식으로 변환하며 하나의 팩에 정적 및 애니메이션 스티커를 모두 지원합니다.

---

## 📄 라이선스 및 면책 조항

이 Colab 노트북은 **MoeStickersBot**의 편의성 래퍼이며, 이는 **GNU General Public License v3.0 (GPL‑3.0)** 에 따라 라이선스가 부여됩니다.

> [!WARNING]
> **면책 조항**: 이 노트북은 귀하의 개인 텔레그램 봇 토큰과 (선택적으로) ngrok 인증 토큰을 사용합니다. 토큰을 안전하게 보관할 책임은 귀하에게 있습니다. 저자는 오용이나 우발적 노출에 대해 책임을 지지 않습니다.

---

## 💕 크레딧 및 감사 인사

### 🌟 원본 프로젝트

이 노트북은 **[Star-39](https://github.com/Star-39)** 님과 **[MoeStickersBot](https://github.com/Shineii86/MoeStickersBot)** 의 모든 기여자분들의 놀라운 작업을 기반으로 합니다. 그들에게 애정을 보내주세요!

### 📓 Colab 노트북 작성자

Google Colab 적응은 **[Shinei Nouzen](https://github.com/Shineii86)** 님이 ❤️를 담아 제작했습니다.  
이 노트북이 도움이 되셨다면 ⭐를 주시고 더 많은 Colab 프로젝트를 위해 팔로우해 주세요!

### 🛠️ 도구 및 라이브러리

- [MoeStickersBot](https://github.com/Shineii86/MoeStickersBot) — 핵심 텔레그램 봇 (Go)
- [ImageMagick](https://imagemagick.org/) — 이미지 처리
- [ffmpeg](https://ffmpeg.org/) — 비디오 변환
- [exiv2](https://exiv2.org/) — 메타데이터 처리
- [ngrok](https://ngrok.com/) — WebApp용 보안 터널
- [Google Colab](https://colab.research.google.com/) — 무료 클라우드 런타임
- [tqdm](https://github.com/tqdm/tqdm) — 진행률 표시줄

---

<div align="center">

### 💕 프로젝트 지원하기

⭐ **[Shineii86/MoeStickersBot에 별 주기](https://github.com/Shineii86/MoeStickersBot)**  
⭐ **[이 Colab 노트북에 별 주기](https://github.com/Shineii86/MoeStickerBot)**

<br>

<a href="https://github.com/Shineii86">
  <img src="https://img.shields.io/badge/Follow-@Shineii86-181717?style=for-the-badge&logo=github" alt="Shineii86 팔로우">
</a>
<a href="https://telegram.me/Shineii86">
  <img src="https://img.shields.io/badge/Telegram-@Shineii86-2CA5E0?style=for-the-badge&logo=telegram" alt="Telegram">
</a>

<img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=gradient&fontAlignY=30&section=footer">

<sup><b>원본 봇 저작권 © Star-39 및 기여자. GPL‑3.0 라이선스.<br>Colab 적응 © Shinei Nouzen. 모든 권리 보유.</b></sup>

</div>
