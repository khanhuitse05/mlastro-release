# MLAstro Landing Page

Official landing page and download portal for **MLAstro Hub** — the next-generation controller for OnStepX-powered telescope mounts.

Live Site: [mlastro.com](https://mlastro.com/)

---

## Overview

This repository contains the static web pages and configuration files serving the MLAstro Hub product page:
- **`index.html`**: Main landing page featuring product highlights, direct download links (iOS App Store, Google Play, Windows desktop installer), and hardware drivers/plugins (CP2102 USB driver, OnStepX ASCOM driver, RPA Nina plugin).
- **`policy.html`**: Privacy policy.
- **`terms.html`**: Terms of service.
- **`windows_config.json`**: Remote configuration and version checks for the desktop client.
- **`assets/`**: Brand assets, icons, screenshots, and artwork.

## Tech Stack

- **HTML5 & Vanilla JavaScript**
- **Tailwind CSS** (via CDN)
- **WebGL** (custom background starfield / nebula shader)
- **Google Fonts & Material Symbols**

## Local Development

Serve the root directory with any local static HTTP server:

```bash
# Using Python
python3 -m http.server 8000

# Or using Node / npx
npx serve .
```

Open [http://localhost:8000](http://localhost:8000) in your browser.

## Deployment

The site is hosted on **Firebase Hosting** and configured in [`firebase.json`](./firebase.json).

### Automated Deployment
Pushes to the `main` branch automatically deploy to Firebase Hosting via the GitHub Actions workflow in [`.github/workflows/firebase_deploy.yml`](./.github/workflows/firebase_deploy.yml).

### Manual Deployment
```bash
firebase deploy --only hosting
```
