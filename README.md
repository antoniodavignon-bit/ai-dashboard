# Dash — Content Engine
> Feed it once. Get a week of content.

![Status](https://img.shields.io/badge/status-active-orange) ![Built by](https://img.shields.io/badge/built%20by-Davignon%20Media%20Group-orange) ![License](https://img.shields.io/badge/license-private-red)

---

## What it is

Dash is a single-file AI-powered content engine built for creators, founders, and community operators who are done staring at a blank screen.

Drop in your niche, your audience, and your offer. Dash connects to a local AI model (via Ollama) and generates a full week of content — hooks, video scripts, platform captions, and a 7-day posting schedule — in one shot.

No subscriptions. No OpenAI API bills. Runs on your own machine.

---

## What it generates

| Stage | Output |
|-------|--------|
| 01 — Hooks | 8 scroll-stopping video openers (curiosity, bold claim, contrarian, story, and more) |
| 02 — Scripts | 2 complete 30–45 sec video scripts with hook, beats, and CTA |
| 03 — Captions | Platform-native captions with hashtags for every selected channel |
| 04 — Schedule | 7-day posting calendar with platform, content type, and idea per day |

---

## Tech stack

- **Frontend** — Pure HTML/CSS/JS, zero dependencies, single file
- **AI Backend** — [Ollama](https://ollama.ai) running locally on your machine
- **Model** — Any Ollama-compatible model (default: `llama3`, recommended: `qwen2.5-coder:7b`)
- **Remote access** — ngrok tunnel (for sharing with members)
- **Fonts** — Bricolage Grotesque, Inter, Space Mono via Google Fonts

---

## Prerequisites

- macOS (M1/M2/M3/M4) recommended
- [Ollama](https://ollama.ai) installed and running
- A pulled model (`ollama pull llama3` or `ollama pull qwen2.5-coder:7b`)
- A browser (Chrome/Safari/Firefox)

---

## Quickstart (local)

```bash
# 1. Pull a model if you haven't
ollama pull llama3

# 2. Start Ollama (if not already running)
ollama serve

# 3. Open the file in your browser
open dash.html
```

4. Leave the endpoint as `http://localhost:11434`
5. Hit **Test connection** — you should see your installed models
6. Fill in your niche, audience, and offer → hit **Generate content plan**

---

## Using with ngrok (for remote members)

```bash
# Start Ollama
ollama serve

# In a new terminal, expose port 11434
ngrok http 11434
```

Copy the `https://...ngrok-free.app` URL → paste it into the **AI endpoint** field in Dash.

> ⚠️ **Privacy note:** When routing through ngrok, prompts pass through ngrok's servers before reaching your local model. For full local privacy, use localhost only.

---

## Supported platforms

Select any combination when generating:

- TikTok
- Instagram Reels
- YouTube Shorts
- Pinterest
- X / Twitter
- LinkedIn

---

## Customization

All prompts live in the `PROMPTS` object in the `<script>` block. Each stage (hooks, scripts, captions, schedule) has its own prompt function that accepts your input context. Edit freely to match your brand voice or niche requirements.

---

## Part of DMG

Dash is a flagship product of **Davignon Media Group LLC** — built for the Maestro Inner Circle community.

- 🛒 Store → [digitaldashers2.com](https://digitaldashers2.com)
- 🏫 Community → Maestro Community on Skool
- 🎓 Education → Maestro University

---

## Roadmap

- [ ] Move off ngrok → serverless proxy backend for true end-to-end privacy
- [ ] Model selector dropdown (auto-detect installed Ollama models)
- [ ] Export to Notion / Google Docs
- [ ] Save + reload past content plans
- [ ] Multi-language support

---

## License

Private — built and owned by Davignon Media Group LLC. Not open source.
