# Spy
### A Claude Code and Codex Skill by [@tenfoldmarc](https://www.instagram.com/tenfoldmarc)

Give it your competitors' Instagram handles and it tells you exactly what's working — which hooks went viral, why they worked, and gives you ready-to-use templates you can steal for your own content. No setup, no database, instant results.

---

## What It Does

1. **Scrapes** your competitors' last 50 Instagram posts each
2. **Finds outliers** — posts that got 5x+ their normal views (the ones that actually went viral)
3. **Downloads and transcribes** each viral reel to extract the spoken hook
4. **Screenshots** the first frame to capture the on-screen text hook
5. **Templatizes** every hook into a reusable `[BRACKET]` framework you can adapt to any topic
6. **Ranks** all templates by total views and tells you which ones work for reels AND carousels
7. **Explains** why each hook works psychologically — so you understand the mechanism, not just the words

---

## Requirements

- A Mac, Linux, or Windows computer
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and working
- An [Apify](https://apify.com) account (free tier works) for Instagram scraping
- `yt-dlp` for downloading reels
- `whisper` for transcription
- `ffmpeg` for screenshots

Don't worry about connecting these manually — the skill walks you through everything on first run.

---

## Install

### Codex on macOS

```bash
git clone https://github.com/JSNGe/spy-skill ~/.codex/skills/spy
```

Start a new Codex turn after installation so the skill catalog refreshes. Invoke it with:

```text
$spy @competitor1 @competitor2 @competitor3
```

The Codex-compatible fork changes the config path to `~/.codex/skills/spy/config.json`, discovers
the Apify tools actually available in the current host instead of assuming Claude-specific MCP tool
names, and uses an isolated temporary directory for downloaded Reels.

### Claude Code

### Step 1 — Open your terminal

**Mac:** Press `Command + Space`, type **Terminal**, hit Enter.
**Windows:** Press `Win + R`, type **cmd**, hit Enter. (If you have Git Bash, use that instead.)
**Linux:** Open your terminal app.

### Step 2 — Run this command

Copy-paste this entire line and hit Enter:

```bash
git clone https://github.com/tenfoldmarc/spy-skill ~/.claude/skills/spy
```

Wait for it to finish (takes a few seconds).

### Step 3 — Open Claude Code

In the same terminal window, type:

```bash
claude
```

Hit Enter.

### Step 4 — Run the skill

Type:

```
/spy @competitor1 @competitor2 @competitor3
```

Replace with real Instagram handles. On your first run, the skill checks for required tools and walks you through installing anything that's missing.

---

## Usage

**Basic — spy on 3 competitors:**
```
/spy @hormozi @garyvee @danmartell
```

**From URLs:**
```
/spy https://www.instagram.com/hormozi/ https://www.instagram.com/garyvee/
```

**Any niche works — AI, fitness, marketing, ecommerce, cooking, whatever:**
```
/spy @drjasonfung @hubaborhealth @glucose_goddess
```

The skill auto-detects the niche from the content it finds.

---

## What You Get

For every viral outlier, you get three hooks + three templates:

- **Spoken hook** — what they actually said in the first 3 seconds
- **On-screen text hook** — what text was displayed on the video
- **Caption hook** — what they wrote in the post caption
- **Templates** — each hook abstracted into a `[BRACKET]` framework you can fill in with your own topic

Plus a **Template Leaderboard** showing which patterns are working across multiple creators, ranked by total views.

---

## Updating

To get the latest version:

```bash
cd ~/.claude/skills/spy && git pull
```

For the Codex-compatible fork:

```bash
cd ~/.codex/skills/spy && git pull
```

---

## Want More?

`/spy` is a one-shot analysis. If you want a **living database** that auto-refreshes every week and builds a growing library of proven hooks, check out [`/hook-intel`](https://github.com/tenfoldmarc/hook-intel-skill).

---

## Built By

[@tenfoldmarc](https://www.instagram.com/tenfoldmarc) — Follow for daily AI automation walkthroughs. Real systems, not theory.

## Upstream and licensing note

This repository is a GitHub fork of
[`tenfoldmarc/spy-skill`](https://github.com/tenfoldmarc/spy-skill), initially based on commit
`6c1dd4dae7e6ff6238c35727e8ef8c6967f8373e`. The upstream author and GitHub fork relationship are
preserved.

The upstream repository did not include a LICENSE file at that revision. Public source code without
a license should not be described as open source or assumed to grant reuse rights beyond GitHub's
fork functionality. No license has been invented or added here.
