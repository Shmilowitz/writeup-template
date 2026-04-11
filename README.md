# Writeup Template

A Jekyll-based CTF/security writeup template with a dark cyberpunk aesthetic, sticky sidebar TOC, image lightbox, and scroll-spy navigation.

---

## Getting Started

### Step 1 — Use this template

Click **"Use this template"** on GitHub to create a new repository from this template. Give it a name that matches your writeup, e.g. `writeup-hackthebox-machine`.

---

### Step 2 — Configure `_config.yml`

This is the only file you need to edit to set up a new writeup. Open `_config.yml` and fill in every field:

```yaml
# Your name — shown in nav, badges, and footer
author: "Your Name"

# The page title shown in the browser tab
title: "YOUR WRITEUP TITLE"

# A short description for social sharing previews
description: "Short description of this writeup"

# GitHub Pages URL — must match your repo
baseurl: "/your-repo-name"
url:     "https://your-username.github.io"

# Hero section — the big text on the front page
hero_eyebrow:  "CTF // Event Name"
hero_title:    "YOUR"
hero_subtitle: "WRITEUP TITLE"

# Metadata badges shown below the hero title
badge_target: "target-hostname"   # e.g. root@server
badge_steps:  "5"                 # number of steps/stages
badge_status: "Complete"          # e.g. In Progress / Complete

# Link to your portfolio site
portfolio_url: "https://your-username.github.io/portfolio"

# Your GitHub repo (used in footer link)
github_repo: "your-username/your-repo-name"
```

---

### Step 3 — Set up the navigation links

In `_config.yml`, edit `nav_links` to match the sections in your writeup. Each item needs a `label` (displayed text) and an `anchor` (the `#id` of the heading it links to):

```yaml
nav_links:
  - label: "Overview"
    anchor: "#overview"
  - label: "Recon"
    anchor: "#recon"
  - label: "Exploit"
    anchor: "#exploit"
  - label: "Conclusion"
    anchor: "#conclusion"
```

---

### Step 4 — Set up the sidebar table of contents

Edit `toc_links` to list every section you want in the sidebar. Add an optional `step` label (e.g. `"01"`) for numbered steps:

```yaml
toc_links:
  - label: "Overview"
    anchor: "#overview"
  - label: "Reconnaissance"
    anchor: "#reconnaissance"
    step: "01"
  - label: "Initial Access"
    anchor: "#initial-access"
    step: "02"
  - label: "Privilege Escalation"
    anchor: "#privilege-escalation"
    step: "03"
  - label: "Conclusion"
    anchor: "#conclusion"
```

The sidebar automatically highlights your current position as you scroll.

---

### Step 5 — Write your content in `README.md`

All writeup content goes in `README.md` using standard Markdown. The headings you use must match the anchors you set in `_config.yml`.

**Headings** — use `##` for main sections and `###` for subsections:

```markdown
## Overview

Introduce the target and the goal of the assessment.

## Reconnaissance

### Port Scanning

Describe what you found.

## Initial Access
```

> The `id` Jekyll generates from `## My Section` is `#my-section` (lowercase, spaces become dashes).

**Code blocks** — fenced code blocks are rendered with a `TERMINAL` label and red left border:

```markdown
    ```bash
    nmap -sV -p- 10.0.0.1
    ```
```

**Images** — place images in `assets/images/` and reference them with a relative path. Clicking an image opens it in the lightbox:

```markdown
![Alt text](assets/images/screenshot.png)
```

**Blockquotes** — use for key findings or flags:

```markdown
> **Flag:** `FLAG{example_flag_here}`
```

---

### Step 6 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Open **Settings → Pages**
3. Under **Branch**, select `main` and `/ (root)`, then click **Save**
4. Your writeup will be live at `https://your-username.github.io/your-repo-name/` within a minute or two

---

### Step 7 — Update the OG image (optional)

Replace `assets/images/og-image.png` with a custom 1200×630px image. This is shown when you share the link on social platforms or in messaging apps.

---

## Features

| Feature | Details |
|---|---|
| Image lightbox | Click any image to expand it full-screen. Press `Esc` or click outside to close. |
| Scroll-spy TOC | The sidebar highlights the section you are currently reading. |
| Mobile layout | Sidebar hides on small screens, font sizes scale down gracefully. |
| Code blocks | Rendered with a `TERMINAL` label and syntax highlighting via Rouge. |
| Dark theme | Full dark cyberpunk aesthetic — no configuration needed. |
