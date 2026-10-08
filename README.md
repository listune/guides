# Listune Documentation

Official end-user documentation website for the Listune Discord Music Bot ecosystem, built with [Retype](https://retype.com).

Live Documentation: [https://docs.listune.app](https://docs.listune.app)

---

## Overview

This repository contains the complete documentation source files for Listune. The documentation covers Discord slash and prefix commands, the synchronized Web Player, server dashboard configuration, 26 real-time audio filters, Discord Embedded Activities, Premium subscription tiers, and troubleshooting guides.

The documentation is configured with Listune brand styling (dark background `#090b0e`, `#13171f` and pink accent `#ec4899`), customized typography, and distinct vector navigation icons.

---

## Directory Structure

```text
docs/
├── .gitignore               # Git ignore rules for Retype builds and artifacts
├── README.md                # Project documentation overview
├── retype.yml               # Retype project configuration and global metadata
├── index.md                 # Documentation homepage and feature navigation
├── favicon.ico              # Listune brand favicon
├── _includes/               # Injected headers, Listune Dark theme, and scripts
│   └── head.html            # Brand stylesheet and dark mode lock
├── assets/                  # Verified images, video demonstrations, and brand assets
│   ├── brand/               # Official SVG logos and identity assets
│   ├── custom-profile-bot.png
│   ├── guild-setting.png
│   ├── guild-stats.png
│   ├── listune-brand-white.webm
│   ├── play-query-link-playlist.png
│   ├── play-query-text.png
│   ├── setup-player-control-embed.gif
│   └── webplayer.gif
├── getting-started/         # Installation guide, invite link, and permissions
│   ├── index.md
│   ├── bot-invite.md
│   ├── permissions.md
│   └── first-playback.md
├── commands/                # Complete 100-command index and syntax guides
│   ├── index.md
│   ├── all-commands.md
│   ├── music-playback.md
│   ├── queue-management.md
│   ├── filters-audio.md
│   ├── playlists.md
│   ├── server-settings.md
│   └── utility-info.md
├── playback/                # Audio engines, supported sources, and filters
│   ├── index.md
│   ├── supported-sources.md
│   ├── queue-controls.md
│   └── audio-filters.md
├── dashboard/               # Server dashboard portal and guild management
│   ├── index.md
│   ├── login-access.md
│   ├── guild-settings.md
│   ├── player-embed-editor.md
│   └── statistics.md
├── web-player/              # Synchronized browser player and live lyrics
│   ├── index.md
│   ├── real-time-controls.md
│   └── live-lyrics.md
├── activities/              # Discord Embedded Activity setup and usage
│   ├── index.md
│   └── voice-dms.md
├── premium/                 # Free vs Premium tiers and Patreon activation
│   ├── index.md
│   ├── tier-comparison.md
│   ├── patreon-activation.md
│   └── 24-7-mode.md
├── voting/                  # Top.gg voting and vote-locked privileges
│   ├── index.md
│   └── voter-privileges.md
├── troubleshooting/         # Diagnostic workflows and common issue resolutions
│   ├── index.md
│   ├── audio-issues.md
│   ├── connection-issues.md
│   └── permission-issues.md
└── resources/               # Official ecosystem destinations and assets
    └── index.md
```

---

## Local Development

### Prerequisites

* [Node.js](https://nodejs.org/) (version 18.0.0 or later)
* npm, pnpm, or yarn

### Running the Live Development Server

From inside the `docs/` directory:

```bash
npx retypeapp start
```

Or if running from the project root:

```bash
npx retypeapp start docs
```

The live server will start at `http://localhost:5001/` with automatic hot reloading upon editing any markdown or styling file.

### Building Static Files

To compile the production static website:

```bash
npx retypeapp build
```

Or from the project root:

```bash
npx retypeapp build docs
```

The output bundle will be generated inside the `.retype/` directory.

---

## Deployment

### GitHub Actions (GitHub Pages)

To automatically publish the documentation to GitHub Pages on every push to the `main` branch, create `.github/workflows/docs.yml`:

```yaml
name: Publish Documentation

on:
  push:
    branches:
      - main
    paths:
      - 'docs/**'

jobs:
  publish:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 20

      - name: Build Documentation
        run: npx retypeapp build docs

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: docs/.retype
```

### Static Hosting (Cloudflare Pages / Vercel / Nginx)

1. Build command: `npx retypeapp build docs`
2. Output directory: `docs/.retype`

---

## Retype Configuration

Global settings are defined in [retype.yml](retype.yml):

* **Title**: Listune
* **Branding**: Official Listune logo and badge
* **Navigation Links**: Quick access to Web App, Invite, Support Server, and Premium
* **Footer**: Copyright notices and legal policy links
* **Theme Customization**: [docs/_includes/head.html](_includes/head.html) enforces brand dark colors (`#090b0e`, `#13171f`, `#ec4899`) and maintains a consistent dark mode experience.

---

## Official Links

* Website: [https://listune.app](https://listune.app)
* Dashboard: [https://listune.app/servers](https://listune.app/servers)
* Documentation: [https://docs.listune.app](https://docs.listune.app)
* Brand Book: [https://brandbook.listune.app](https://brandbook.listune.app)
* Discord Bot Invite: [https://listune.app/invite](https://listune.app/invite)
* Discord Support Server: [https://discord.gg/Bxrj3CYvPK](https://discord.gg/Bxrj3CYvPK)
* Top.gg Voting: [https://listune.app/topgg](https://listune.app/topgg)
* Patreon: [https://www.patreon.com/c/listune](https://www.patreon.com/c/listune)

---

## License

Copyright 2026 Listune. All rights reserved.
