# UKOAPP — Static Landing Page

This repository hosts the static landing page for **ukoapp.com**, deployed via GitHub Pages.

## Structure
- `index.html` — Main landing page  
- `404.html` — Custom error page  
- `robots.txt` — Crawler directives  
- `CNAME` — Custom domain configuration  
- `.nojekyll` — Disables Jekyll to ensure static file serving

## Security
- `main` branch is protected  
- Direct pushes are disabled  
- All changes must go through a Pull Request  
- No secrets, no backend, no external scripts  
- GitHub Actions disabled for maximum security

## Deployment
GitHub Pages automatically deploys from the `main` branch.

## Workflow
1. Create a new branch  
2. Commit changes  
3. Open a Pull Request  
4. Merge into `main`  
5. Delete the temporary branch
