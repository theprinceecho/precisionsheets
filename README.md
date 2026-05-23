# PrecisionSheets

**Professional-grade Excel tools and dashboards for finance professionals who value clarity, precision, and calm decision-making.**

## Live Site

- [precisionsheets.info](https://precisionsheets.info)

## Overview

PrecisionSheets provides clean, ready-to-use Excel templates designed for real-world financial work. The tools are built to work seamlessly whether you are on the go or back at your desk, and are structured to be easily combined with your own data and Chart of Accounts.

## GitHub CI/CD Architecture

This repository uses a clean and lightweight CI/CD setup:

- **CI Workflow**: Runs HTMLHint linting on every push and pull request
- **Deploy Workflow**: Automatically publishes the site to GitHub Pages on push to `main`

![GitHub CI/CD Workflow Chart](assets/github-ci-cd-workflow-chart.jpg)

## Project Structure

```
.
├── index.html
├── contact.html
├── legal.html
├── .github/workflows/
│   ├── ci.yml
│   └── deploy.yml
├── .htmlhintrc
├── .nojekyll
└── README.md
```

## CI / CD Details

### CI Workflow (`.github/workflows/ci.yml`)
- Triggers: Push to `main` + Pull Requests
- Runs **HTMLHint** for HTML quality checks
- Ensures code consistency before merging

### Deployment Workflow (`.github/workflows/deploy.yml`)
- Triggers: Push to `main`
- Deploys the static site to **GitHub Pages** using modern deployment

## Local Development

No build step required. Open `index.html` in any modern browser.

## Contributing

We follow a disciplined approach:
- Think before making changes
- Keep modifications minimal and focused
- Ensure HTML linting passes

Open a pull request once your changes are ready.