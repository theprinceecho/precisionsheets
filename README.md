# PrecisionSheets

**Professional-grade Excel tools and dashboards for finance professionals who value clarity, precision, and calm decision-making.**

## Live Site

- [precisionsheets.info](https://precisionsheets.info)

## Overview

PrecisionSheets provides clean, ready-to-use Excel templates designed for real-world financial work. The tools are built to work seamlessly whether you are on the go or back at your desk, and are structured to be easily combined with your own data and Chart of Accounts.

## Project Structure

```
.
├── index.html          # Main landing page
├── contact.html        # Contact form
├── legal.html          # Legal disclosure
├── .github/workflows/  # CI/CD workflows
├── .htmlhintrc         # HTML linting configuration
└── .nojekyll           # GitHub Pages configuration
```

## CI / CD

This project uses GitHub Actions for quality assurance and automated deployment:

### CI Workflow (`.github/workflows/ci.yml`)
- Runs on every push and pull request
- Performs HTML linting using **HTMLHint**
- Helps maintain code quality and consistency

### Deployment Workflow (`.github/workflows/deploy.yml`)
- Automatically deploys the site to GitHub Pages on every push to `main`
- Uses the modern GitHub Pages deployment method

## Local Development

No build step is required. Simply open `index.html` in any modern browser.

## Contributing

1. Make your changes
2. Ensure the HTML linting checks pass (CI will run automatically on PRs)
3. Open a pull request

We follow a "think before changing" and "simplicity first" approach. Please keep changes focused and minimal.