# Jikimi

Privacy-first parental controls. Screen time management, DNS filtering, 
AI-powered content analysis, and on-device OCR — all without sending 
your family's data to an ad company.

## Status

The codebase is being prepared for open source release. 
Client source will be published here when ready.

- **Features**: [jikimi.app/features](https://jikimi.app/features)
- **Roadmap**: [jikimi.app/roadmap](https://jikimi.app/roadmap)
- **Download (Linux)**: [jikimi.app/download](https://jikimi.app/download)
- **Windows client**: Coming soon
- **macOS client**: On the roadmap

## Features

### Screen Time & Scheduling
- Daily time limits with weekday/weekend differentiation
- Bedtime and school hours schedules
- Per-app and per-category time caps
- Bonus time rewards for positive behaviour
- Time request system — kids ask, parents approve/deny remotely
- Instant pause across all devices from the dashboard

### Content Filtering
- DNS-level filtering with AI-powered domain categorisation (Claude)
- 11 content categories (adult, violence, gambling, drugs, hate speech, etc.)
- Safe search enforcement across Google, Bing, YouTube, DuckDuckGo
- Custom block/allow lists and temporary exceptions
- Age-grouped filter profiles (0-4, 5-9, 10-12, 13-15, 16-17, 18+)

### On-Device AI & Monitoring
- Screen text extraction via PaddleOCR — processed locally, no screenshots leave the device
- Keystroke sentiment analysis for detecting bullying, grooming, and emotional distress
- Urgency-level alerts (low to critical) with context-aware interpretation
- Audio and media playback detection
- Browser history tracking (domain names only, never full URLs or page content)

### Game Detection
- Automatic detection across Steam, Epic, GOG, Lutris, Wine/Proton, Flatpak, Snap
- Native Linux games, emulators (RetroArch, Dolphin), game engines (Unity, Unreal, Godot)
- Game category classification with confidence scoring
- Unidentified game telemetry for continuous improvement

### Enforcement & Tamper Protection
- Full-screen lock overlay when time expires
- Process termination for apps exceeding limits
- Anti-tamper detection (debugger attachment, library injection, environment tampering)
- Watchdog service with automatic crash recovery
- Systemd integration with encrypted configuration storage

### Parent Dashboard & Communication
- Unified dashboard for all children and devices
- Two-way parent-child messaging
- Real-time alerts with severity prioritisation
- Remote device control (pause, block, unlock, extend time)
- Activity reports with trend analysis (daily, weekly, monthly)
- Webhook integrations for custom alerting

### Privacy & Security
- All OCR and sentiment analysis runs on-device
- Only domain names collected, never full URLs or page content
- No screenshots, photos, GPS, or password logging
- Encrypted communication (TLS) and encrypted storage at rest

### Developer API & AI Integration
- **REST API (v2)** — scoped API keys for building custom dashboards and automations
- **Parent MCP Server** — manage screen time, alerts, and messaging through AI assistants like Claude
- **Child MCP Server** — children can check their time, request extensions, and message parents via AI
- **Website MCP Server** — public, unauthenticated access to product info, pricing, and docs
- 17 parent tools, 7 child tools, 8 product info tools
- Webhook support for event-driven integrations
- Full interactive API docs at `/api/docs`
- Developer portal: [jikimi.app/developers](https://jikimi.app/developers)

### Platform & Integration
- Rust client — native performance, not an Electron wrapper
- GTK4 desktop UI with system tray integration
- 20 language localisation
- Automatic client updates with version management
- Offline queuing with sync when reconnected

## Contact

Questions or feedback? Open a discussion or reach out at [jikimi.app](https://jikimi.app).
