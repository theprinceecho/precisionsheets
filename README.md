# PrecisionSheets

**Professional-grade Excel tools and dashboards for finance professionals who value clarity, precision, and calm decision-making.**

## Live Site

- [precisionsheets.info](https://precisionsheets.info)

## Overview

PrecisionSheets provides clean, ready-to-use Excel templates designed for real-world financial work. The tools are built to work seamlessly whether you are on the go or back at your desk, and are structured to be easily combined with your own data and Chart of Accounts.

## GitHub CI/CD Architecture

This repository uses a clean and lightweight CI/CD setup:

- **PR Checks Workflow**: Runs HTMLHint + Lighthouse CI on Pull Requests
- **Deploy Workflow**: Automatically publishes the site to GitHub Pages on push to `main`

![GitHub CI/CD Workflow Chart](assets/github-ci-cd-workflow-chart.jpg)

### GitHub Setup Status

| Component                  | File / Path                                  | Status    | Purpose                                              |
|---------------------------|----------------------------------------------|-----------|------------------------------------------------------|
| **PR Checks Workflow**    | `.github/workflows/pr-checks.yml`            | 🟢 Active | HTML Linting + Lighthouse CI on Pull Requests        |
| **Deploy Workflow**       | `.github/workflows/deploy.yml`               | 🟢 Active | Automatic deployment to GitHub Pages                 |
| **HTML Linting Config**   | `.htmlhintrc`                                | 🟢 Active | Defines HTML quality & accessibility rules           |
| **Lighthouse Config**     | `lighthouserc.json`                          | 🟢 Active | Lighthouse CI configuration (Performance, A11y, SEO) |
| **GitHub Pages Config**   | `.nojekyll`                                  | 🟢 Active | Prevents Jekyll processing on static HTML            |
| **Documentation**         | `README.md`                                  | 🟢 Active | Project overview + CI/CD documentation               |
| **Workflow Chart**        | `assets/github-ci-cd-workflow-chart.jpg`     | 🟢 Active | Visual reference of the full GitHub setup            |

## Project Structure

```
.
├── index.html
├── contact.html
├── legal.html
├── .github/workflows/
│   ├── pr-checks.yml
│   └── deploy.yml
├── lighthouserc.json
├── .htmlhintrc
├── .nojekyll
└── README.md
```
## GitHub Pages Deployment

This repository uses **GitHub Actions** as the deployment source for GitHub Pages (not "Deploy from a branch").

### Current Configuration
- **Source**: GitHub Actions
- **Custom Domain**: `precisionsheets.info`
- **Enforce HTTPS**: Enabled

### Why We Use GitHub Actions

We have a dedicated deployment workflow (`.github/workflows/deploy.yml`) that handles publishing. This is the modern and recommended approach because it:

- Gives full control over when and how the site is deployed
- Uses secure OIDC authentication (no deploy keys required)
- Works cleanly together with our PR Checks workflow (`pr-checks.yml`)

The site is automatically deployed on every push to `main`. You can also manually trigger a deployment from the **Actions** tab → **"Deploy static content to Pages"** workflow.

## CI / CD Details

### PR Checks Workflow (`.github/workflows/pr-checks.yml`)
- Runs **HTML Linting** (HTMLHint) on push + Pull Requests
- Runs **Lighthouse CI** on Pull Requests only (Performance, Accessibility, SEO)
- Strong quality gates before merging

### Deployment Workflow (`.github/workflows/deploy.yml`)
- Triggers automatically on every push to `main`
- Uses modern GitHub Pages deployment with OIDC
- Deploys the entire root folder as the static site

**Manual Deployment**

You can manually trigger a deployment at any time:

1. Go to the **Actions** tab in the repository
2. Select the **"Deploy static content to Pages"** workflow
3. Click **"Run workflow"** → **"Run workflow"**

This is useful if you want to redeploy without pushing new code.

> **Note:** For the deployment workflow to work, GitHub Pages must be set to **Source: GitHub Actions** in the repository settings (Settings → Pages).

## Local Development

No build step required. Open `index.html` in any modern browser.

## Contributing

We follow a disciplined approach:
- Think before making changes
- Keep modifications minimal and focused
- Ensure PR checks pass (HTML + Lighthouse)

Open a pull request once your changes are ready.
