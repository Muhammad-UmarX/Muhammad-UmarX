# GitHub Profile README — Setup Guide

## Quick Start (5 minutes)

### Step 1 — Create Your Profile Repository

1. Go to [github.com/new](https://github.com/new)
2. Set **Repository name** to exactly: `Muhammad-UmarX` (must match your username)
3. Make it **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

> GitHub automatically displays the README.md from a repo that matches your username on your profile page.

---

### Step 2 — Upload All Files

Your profile repo needs this exact structure:

```
Muhammad-UmarX/
├── README.md
├── assets/
│   ├── hero.svg          ← Animated lightning banner
│   ├── divider.svg       ← Lightning section dividers
│   └── terminal.svg      ← About Me terminal card
└── .github/
    └── workflows/
        └── snake.yml     ← Snake animation generator
```

**Upload steps:**
1. Clone your new repo locally or use GitHub's web upload
2. Copy all files from this folder into the repo maintaining the folder structure
3. Commit and push

**Or via command line:**
```bash
git clone https://github.com/Muhammad-UmarX/Muhammad-UmarX.git
cd Muhammad-UmarX
# Copy all files from this folder into the cloned repo
git add -A
git commit -m "Add profile README with animated lightning theme"
git push origin main
```

4. Visit `https://github.com/Muhammad-UmarX` — you should see the animated lightning header, terminal card, stats, and badges!

---

### Step 3 — Set Up the Snake Animation

1. In your repo, go to **Settings** → **Actions** → **General**
2. Under **"Workflow permissions"**, select **"Read and write permissions"**
3. Click **Save**
4. Go to the **Actions** tab
5. Click **"Generate Snake Animation"** in the sidebar
6. Click **"Run workflow"** → **"Run workflow"**
7. Wait ~1 minute for completion
8. The snake SVG will now appear in your README

> The workflow auto-runs every 12 hours to stay updated.

---

## Customization

### Personal Info

Find & Replace these values across **all files** (README.md + SVGs):

| Placeholder | Replace With |
|---|---|
| `Muhammad-UmarX` | Your GitHub username |
| `Muhammad Umar` | Your display name |
| `Venturing the AI Dimension` | Your tagline |
| `YOUR_LINKEDIN_USERNAME` | LinkedIn username |
| `YOUR_TWITTER_HANDLE` | Twitter/X handle |
| `YOUR_PORTFOLIO_WEBSITE` | Portfolio URL |
| `YOUR_EMAIL@example.com` | Your email |

> The hero banner and terminal card SVGs also contain your name and tagline — edit `assets/hero.svg` and `assets/terminal.svg` directly to change them.

---

### Color Theme

The entire profile uses this palette:

| Hex Code | Color | Used For |
|---|---|---|
| `DC143C` | Crimson Red | Primary accent |
| `FF4444` | Bright Red | Secondary accent |
| `FF6B6B` | Soft Red | Subtle accents |
| `0d1117` | Dark | Backgrounds |
| `C9D1D9` | Light Gray | Body text |
| `1a0a0a` | Very Dark Red | Gradients |
| `3d0000` | Dark Red | Gradients |

**Example — switch to electric blue:**
- `DC143C` → `1E90FF`
- `FF4444` → `4DA6FF`
- `FF6B6B` → `87CEEB`
- `3d0000` → `001a3d`
- `1a0a0a` → `0a0a1a`

> Remember to update colors in the SVG files too (`hero.svg`, `divider.svg`, `terminal.svg`).

---

### Typing Animation Text

In `README.md`, find the `readme-typing-svg` URL and edit the `lines` parameter:

```
lines=First+Line;Second+Line;Third+Line
```

- `+` = space
- `;` = separator between lines

---

### Tech Badges

Badge format:
```
![Name](https://img.shields.io/badge/LABEL-BG?style=for-the-badge&logo=LOGO&logoColor=COLOR)
```

Browse available logos at [simpleicons.org](https://simpleicons.org)

---

### Editing the SVG Assets

The SVGs are standard XML files editable in any text editor:

- **hero.svg** — Change the name text, tagline, subtitle, lightning bolt paths, or animation timing
- **divider.svg** — Adjust the zigzag pattern, colors, or pulse speed
- **terminal.svg** — Edit any key/value pairs, add new rows, change the terminal title

---

## Troubleshooting

| Issue | Solution |
|---|---|
| SVGs not showing | Make sure the `assets/` folder is committed; check file paths are relative (`./assets/...`) |
| Lightning not animating | SVG animations require a modern browser; they won't animate in GitHub's mobile app |
| Stats cards wrong data | Cached ~30 min; add `&cache_seconds=1800` to force refresh |
| Snake broken image | Run the workflow manually; verify workflow permissions are set to read/write |
| Badges not loading | Check logo names at [simpleicons.org](https://simpleicons.org) |
| Header text too big/small | Edit `font-size` in `assets/hero.svg` |

---

**Made with crimson and code**
