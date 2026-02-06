<p align="center">
  <img src="assets/ix-logo.png" alt="INFINITX AI" width="120" />
</p>

<h1 align="center">IX AI Agent Social Media Manager</h1>

<p align="center">
  <strong>Post to 13 social media platforms by talking to AI.<br/>No dashboards. No scheduling apps. Just conversation.</strong>
</p>

<p align="center">
  <a href="https://app.infinitxai.com/">INFINITX Platform</a> &bull;
  <a href="https://www.youtube.com/@enriquemarq-0">YouTube</a> &bull;
  <a href="https://www.linkedin.com/in/enrique-marq-756191319/">LinkedIn</a> &bull;
  <a href="https://www.instagram.com/kikefuturo_/">Instagram</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platforms-13-4ade80?style=flat-square" alt="13 Platforms" />
  <img src="https://img.shields.io/badge/Setup-5%20min-3b82f6?style=flat-square" alt="5 min setup" />
  <img src="https://img.shields.io/badge/License-MIT-eab308?style=flat-square" alt="MIT License" />
  <img src="https://img.shields.io/badge/Powered%20by-Claude%20Code-8b5cf6?style=flat-square" alt="Claude Code" />
</p>

---

## What Is This?

A set of **Claude Code Skills** that turn Claude into your personal AI social media manager. Tell it what to post, where to post it, and it handles everything — formatting, platform-specific optimization, thumbnails, hashtags, SEO tags, timestamps, and more.

**One conversation. Every platform. Done.**

> Think of it like hiring a social media manager that works 24/7, never forgets to post, handles 13 platforms, and you just talk to them like a colleague.

---

## Supported Platforms

| Platform | Text | Images | Video | Scheduling |
|----------|:----:|:------:|:-----:|:----------:|
| Twitter / X | Yes | Yes | Yes | Yes |
| LinkedIn | Yes | Yes | Yes | Yes |
| Instagram | Yes | Yes | Yes | Yes |
| YouTube | Yes | — | Yes | Yes |
| TikTok | Yes | — | Yes | Yes |
| Facebook | Yes | Yes | Yes | Yes |
| Threads | Yes | Yes | — | Yes |
| Bluesky | Yes | Yes | — | Yes |
| Pinterest | Yes | Yes | Yes | Yes |
| Reddit | Yes | Yes | Yes | Yes |
| Google Business | Yes | Yes | — | Yes |
| Telegram | Yes | Yes | Yes | Yes |
| Snapchat | Yes | Yes | Yes | Yes |

---

## How It Works

```
You (VS Code) --> Claude Code --> Late MCP --> 13 Platforms
```

1. **You talk** to Claude inside VS Code (or terminal)
2. **Claude reads** your skills to know how to format for each platform
3. **Late MCP** connects Claude to your social media accounts
4. **Posts go live** with unique content per platform, every time

---

## What's Inside

```
ix-ai-agent-social-media-manager/
|-- .claude/
|   +-- skills/
|       |-- late-social-media/          # Core multi-platform posting
|       |-- short-form-posting/         # Shorts / Reels / TikTok
|       +-- youtube-content-package/    # Full YouTube workflow
|-- examples/
|   |-- post-to-twitter.md             # Example: text post
|   |-- post-short-form.md             # Example: video to 3 platforms
|   +-- youtube-full-package.md        # Example: full YouTube upload
|-- assets/
|   +-- ix-logo.png
|-- CLAUDE.md                           # AI instructions
+-- README.md
```

### Skills at a Glance

| Skill | What It Does | Platforms |
|-------|-------------|-----------|
| **late-social-media** | Text posts, images, cross-posting, threads, scheduling | All 13 |
| **short-form-posting** | Transcribes video, creates unique captions per platform | YouTube Shorts, Instagram Reels, TikTok |
| **youtube-content-package** | Full YouTube SEO package: title, description, tags, timestamps, first comment, thumbnail | YouTube |

---

## Quick Start

### 1. Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

Or install the **Claude Code extension** in VS Code (search "Claude Code" in Extensions).

### 2. Clone This Repo

```bash
git clone https://github.com/Trejon-888/ix-ai-agent-social-media-manager.git
cd ix-ai-agent-social-media-manager
```

### 3. Get Your Late API Key

1. Go to [getlate.dev](https://getlate.dev) and create a free account
2. Connect your social media accounts from the dashboard
3. Navigate to **Settings > API Keys > Create new key**
4. Copy your API key

### 4. Add the Late MCP Server

```bash
claude mcp add late -- uvx --from 'late-sdk[mcp]' late-mcp
```

Set your API key as an environment variable:

```bash
# Mac / Linux
export LATE_API_KEY=your_key_here

# Windows (PowerShell)
$env:LATE_API_KEY = "your_key_here"
```

### 5. Configure Your Skills

Open each skill file and replace the placeholders with your credentials:

| Placeholder | Where to Find It |
|-------------|-----------------|
| `YOUR_LATE_API_KEY` | Late dashboard > Settings > API Keys |
| `YOUR_YOUTUBE_ACCOUNT_ID` | Ask Claude: *"List my Late accounts"* |
| `YOUR_LINKEDIN_ACCOUNT_ID` | Ask Claude: *"List my Late accounts"* |

Files to update:
- `.claude/skills/late-social-media/SKILL.md`
- `.claude/skills/short-form-posting/SKILL.md`
- `.claude/skills/youtube-content-package/SKILL.md`

### 6. Start Posting

Open Claude Code in this project folder and talk:

```
"Post this to Twitter and LinkedIn: Just shipped a new feature.
AI-powered content distribution. The future is here."
```

Claude formats it for each platform, shows you a preview, asks for confirmation, and posts. Done.

---

## Example Prompts

**Single platform post:**
```
Post to Twitter: "Building in public is the best marketing strategy."
```

**Cross-post to multiple platforms:**
```
Post this to Twitter, LinkedIn, and Threads:
"We just hit 10,000 users. Here's the 3 things we did differently."
```

**Short-form video (3 platforms at once):**
```
Post this video as a YouTube Short, Instagram Reel, and TikTok.
[drag your video file into the chat]
```

**Full YouTube upload with SEO:**
```
Upload this video to YouTube. Create a full content package:
title, description, tags, timestamps, and thumbnail concept.
[drag your video file into the chat]
```

**Schedule a post:**
```
Schedule this for tomorrow at 9am EST on LinkedIn:
"AI doesn't replace marketers. It replaces the parts of marketing
that marketers hate doing."
```

---

## Skills Deep Dive

### late-social-media

The core posting engine. Handles any platform, any format.

- Single and multi-platform posting in one command
- Platform-specific formatting (tone, length, hashtags)
- Image and video media upload
- Thread creation for Twitter and Threads
- Scheduling and draft management
- **Never posts without your explicit approval**

### short-form-posting

Specialized for short-form video content across YouTube Shorts, Instagram Reels, and TikTok.

- Transcribes your video to understand the content
- Creates **unique captions per platform** (professional for YouTube, casual for Instagram, punchy for TikTok)
- Platform-specific hashtags and CTAs
- Thumbnail / cover frame selection
- Posts to all 3 platforms in a single conversation

### youtube-content-package

The complete YouTube workflow — everything you need to publish a professional video.

- Video compression if over 500MB (via FFmpeg)
- Transcript extraction with timestamps
- **5 SEO-optimized title options**
- Full description with timestamps, links, and hashtags
- Tag research across 5 categories (core, outcome, identity, tool, discovery)
- First comment CTA for engagement
- Thumbnail concept generation

---

## Troubleshooting

| Issue | Fix |
|-------|-----|
| "Account not found" | Ask Claude to *"List my Late accounts"* and update skill files with correct IDs |
| "Late MCP not connected" | Run `claude mcp add late -- uvx --from 'late-sdk[mcp]' late-mcp` |
| "Rate limited" | Wait a few seconds and retry. Add delays between bulk posts. |
| Video upload fails | Ensure video is under 500MB. The youtube skill auto-compresses via FFmpeg. |
| Claude doesn't read skills | Open Claude Code **inside this project folder**. Skills are path-dependent. |

---

## About INFINITX AI

<p align="center">
  <a href="https://app.infinitxai.com/">
    <img src="assets/ix-logo.png" alt="INFINITX AI" width="60" />
  </a>
</p>

We don't sell AI tools. We sell transformations.

**[INFINITX AI](https://app.infinitxai.com/)** builds AI systems so you can stay in your zone of genius — closing deals, building relationships, growing your network. The AI handles the rest. $350M+ deal flow track record. 40+ businesses transformed. Real results, documented publicly.

This repo is us giving away the playbook. Because that's how we operate — value first, always.

**See what we're building:** [app.infinitxai.com](https://app.infinitxai.com/)

---

## License

MIT — Use it, fork it, build on it. Take action. If you create something with this, tell us about it.

---

## Built With

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) by Anthropic
- [Late](https://getlate.dev) Social Media API
- [INFINITX AI](https://app.infinitxai.com/)

<p align="center">
  <sub>Much love. Peace. Prosperity. And abundance. — <a href="https://app.infinitxai.com/">INFINITX AI</a></sub>
</p>
