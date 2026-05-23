# PrecisionSheets

Professional landing page and high-quality Excel tools for finance professionals.

## Live Site

- [precisionsheets.info](https://precisionsheets.info)

## Project Structure

- `index.html` — Main landing page
- `contact.html` — Contact form page
- `legal.html` — Legal disclosure
- `.github/workflows/` — CI/CD workflows

## CI / CD

This repository uses GitHub Actions for quality and deployment:

- **CI** (`.github/workflows/ci.yml`): Runs on every push and pull request. Performs HTML linting using HTMLHint.
- **Deploy** (`.github/workflows/deploy.yml`): Automatically deploys the site to GitHub Pages on every push to `main`.

## Local Development

Simply open `index.html` in a browser. No build step required.

## Contributing

Please ensure changes pass the HTML linting checks before merging.