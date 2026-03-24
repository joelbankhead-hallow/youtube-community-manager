# YouTube Community Manager

An AI-powered YouTube comment moderation tool built for the Hallow channel.

## What it does

- **Analyses comments** using Claude AI against your editable moderation guidelines
- **Auto-hearts** positive, faith-affirming comments
- **Drafts replies** in Hallow's voice — you approve, edit, or skip each one before anything posts
- **Flags escalations** (distress, crisis) for human review — no auto-reply
- **Hides spam** automatically

## Live app

👉 [Open the app](https://YOUR-USERNAME.github.io/youtube-community-manager/)

## Setup

### 1. YouTube Data API credentials

You'll need a Google Cloud project with the YouTube Data API v3 enabled and an OAuth 2.0 client ID. Full step-by-step instructions are built into the app's **API Setup** tab.

### 2. Anthropic API key

The app calls the Anthropic Claude API directly from the browser. You'll need a key from [console.anthropic.com](https://console.anthropic.com). Add it in the **API Setup** tab.

> **Note:** Credentials are stored in your browser's `localStorage` only — they are never sent to any server other than YouTube's and Anthropic's own endpoints.

## Running locally

This is a single `index.html` file with no build step. Just open it in any browser:

```bash
open index.html
```

Or serve it locally:

```bash
npx serve .
```

## Deploying

Pushes to `main` automatically deploy to GitHub Pages via the included workflow (`.github/workflows/deploy.yml`).

## Roadmap

- [ ] Real YouTube OAuth token exchange (requires small backend — see notes in app)
- [ ] Scheduled polling for new comments
- [ ] Post approved replies back to YouTube via API
- [ ] Multi-channel support (Maddie's channel, etc.)
- [ ] Export moderation log to CSV

## Tech

- React 18 (via CDN, no build step)
- Claude claude-sonnet-4-20250514 API for comment analysis
- YouTube Data API v3
- GitHub Pages for hosting
