# Threads Auto Like Bot

A production-ready Android automation that auto-likes posts on **Instagram Threads** with human-like pacing, device fingerprint isolation, and queue-based scheduling. It removes the grind of manual engagement while protecting account health using non-ADB wireless control and randomized behavior modeling. The result: steady growth signals for your Threads presence without risking bans or wasting hours tapping like.
<p align="center">
  <a href="https://Appilot.app" target="_blank">
    <img src="media/appilot-baner.png" alt="Appilot Banner" width="100%">
  </a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20Appilot%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:support@appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom Threads Auto Like Bot, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction
This bot automates the process of liking Threads posts on real Android devices and emulators. It targets feeds, hashtags, profiles, or search results and performs safe, human-like interactions with delays, jitters, and scroll variance.

**Context: Automating Threads Engagement Tasks**
- Eliminates repetitive tapping and scrolling while adhering to platform rate limits.
- Supports multi-account rotations with per-account limits and warm-up strategies.
- Works on real devices or emulators with proxy + fingerprint isolation for safety.
- Centralized control via Appilot dashboard for scheduling, monitoring, and logs.
- Designed to scale from a single device to enterprise-grade mobile farms.

## Core Features
- **Real Devices and Emulators:** Run on real Android phones or emulator stacks (Bluestacks/Nox) with identical flows and per-device override configs.
- **No-ADB Wireless Automation:** Control devices through Appilot’s wireless channel (no USB/ADB needed) to reduce detection surface and simplify farm ops.
- **Mimicking Human Behavior:** Randomized delays, scroll speeds, touch offsets, micro-pauses, and session breaks to emulate natural usage patterns.
- **Multiple Accounts Support:** Account pools with session vaults, cooldowns, per-account daily caps, and time windows to keep actions safe.
- **Multi-Device Integration:** Orchestrate 1–1000+ devices with queues, sharded task runners, and per-bucket proxy assignments.
- **Exponential Growth for Your Account:** Consistent, compounding engagement signals on niche feeds to drive impressions and follow-backs.
- **Premium Support:** Priority debugging, device onboarding help, and SLA-backed response windows.

**Additional Capabilities**

| Feature | Description |
|---|---|
| **Targeting Filters** | Like from home feed, specific profiles, search keywords, or hashtag/topic feeds with include/exclude rules. |
| **Safe-Rate Engine** | Adaptive throttling based on feedback (blocks, soft limits, UI errors) and time-of-day schedules. |
| **Proxy & Fingerprint Ops** | Per-device proxy routing and browser/device fingerprint isolation via Multilogin/AdsPower workflows. |
| **Retry & Recovery** | Auto-resume on app crashes, unexpected dialogs, or network hiccups with smart checkpoints. |
| **Run Scheduler** | Cron-like jobs, drip campaigns, and burst modes controlled from Appilot dashboard. |
| **Observability** | Structured logs, session replays (optional), KPI dashboards, and JSON exports. |

</p>
<p align="center">
  <a href="https://appilot.app" target="_blank">
    <img src="media/threads-auto-like-bot-banner.png" alt="threads-auto-like-bot-architecture" width="95%">
  </a>
</p>

## How It Works
1. **Input or Trigger** — Start a job in Appilot by selecting targets (hashtags, profiles, search queries) and setting session duration, daily caps, and concurrency per device/account.  
2. **Core Logic** — The runner controls Android via **UI Automator/Appium** or Appilot’s wireless channel, opens Threads, scrolls feed, detects like buttons with accessibility locators, and taps with randomized offsets and delays.  
3. **Output or Action** — Likes are performed according to rules (e.g., 1 in N posts, skip duplicates, stop on limit), and results (counts, errors, session time) are recorded and pushed to the dashboard.  
4. **Other functionalities** — Built-in retry logic, error classification, structured logging, backoff strategies, and parallel processing across device buckets ensure stable throughput and easy troubleshooting.

## Tech Stack 
- **Language:** Kotlin, Java, Python, JavaScript  
- **Frameworks:** Appium, UI Automator, Espresso, Robot Framework, Cucumber  
- **Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks, Nox Player, Scrcpy, Firebase Test Lab, MonkeyRunner, Accessibility  
- **Infrastructure:** Dockerized device farms, Cloud-based emulators, Proxy networks, Parallel Device Execution, Task Queues, Real device farm

## Directory Structure
```
threads-auto-like-bot/
│
├── src/
│ ├── main.py
│ ├── bot/
│ │ ├── runner.py
│ │ ├── threads_client.py
│ │ ├── selectors.py
│ │ ├── behaviors/
│ │ │ ├── like_flow.py
│ │ │ ├── scroll_variants.py
│ │ │ └── throttling.py
│ │ └── utils/
│ │ ├── logger.py
│ │ ├── proxy_manager.py
│ │ ├── device_registry.py
│ │ └── config_loader.py
│ ├── workers/
│ │ ├── queue_worker.py
│ │ └── scheduler.py
│ └── api/
│ ├── server.js
│ └── routes/
│ └── jobs.ts
│
├── config/
│ ├── settings.yaml
│ ├── accounts.csv
│ ├── targets.yaml
│ └── credentials.env
│
├── tests/
│ ├── unit/
│ │ └── test_throttling.py
│ └── e2e/
│ └── test_like_flow.robot
│
├── logs/
│ ├── runner.log
│ └── device/
│ └── device-001.log
│
├── output/
│ ├── sessions.json
│ └── reports/
│ └── daily_summary.csv
│
├── docker/
│ ├── docker-compose.yaml
│ └── farm.Dockerfile
│
├── requirements.txt
├── package.json
└── README.md
```
## Use Cases
- **Creators** use it to like within their niche feeds, so they can trigger more impressions and community visibility.  
- **Agencies** use it to run multi-account campaigns, so they can deliver measurable engagement for clients at scale.  
- **Growth teams** use it to warm up fresh accounts, so they can reduce blocks and reach safe daily action velocity.  
- **Researchers** use it to run controlled interaction experiments, so they can study feed response to engagement patterns.  

## FAQs
**How do I configure this for multiple accounts?**  
Import `accounts.csv` with per-account caps and schedules. The scheduler picks accounts in round-robin, respects cooldowns, and halts any account hitting a soft limit.

**Does it support proxy rotation or anti-detection?**  
Yes. Assign a dedicated proxy per device/account and integrate with your fingerprint container (e.g., Multilogin/AdsPower) to keep identities isolated.

**Can I schedule it to run periodically?**  
Use the Appilot dashboard to create cron-like schedules (daily windows, night mode, bursts). Jobs auto-pause during risk hours and resume within defined windows.

**What targeting options are available?**  
Home feed, hashtag/topic feeds, profile timelines, and keyword search results, with skip rules (private accounts, duplicates, already liked, etc.).

**Will it work without USB/ADB?**  
Yes. The preferred mode is Appilot’s no-ADB wireless control. ADB/USB fallback is available for debugging and certain device farms.

## Performance & Reliability Benchmarks
- **Execution Speed:** 180–320 safe likes per account per day in drip mode (adaptive to risk signals and time windows).  
- **Success Rate:** 95% end-to-end task completion across stable networks with recommended device prep.  
- **Scalability:** Proven orchestration patterns for **300–1000 devices** using sharded queues and per-bucket proxies.  
- **Resource Efficiency:** Lightweight runners (~100–200MB RAM per worker) with batched UI reads and minimal screenshot frequency.  
- **Error Handling:** Categorized retries (UI-not-found, network, auth), exponential backoff, circuit breakers on repeated failures, and alerting to Slack/Telegram.

##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>

