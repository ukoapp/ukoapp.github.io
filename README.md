# UKOAPP — Static Landing Website (GitHub Pages)

This repository hosts the static landing website for **UKOAPP**, deployed through  
GitHub Pages. The site is intentionally minimalistic, fully static, and designed  
for maximum security, stability, and simplicity.

---

## 1. Project Architecture

The website uses a deliberately simple structure:

- `index.html` — main page
- `404.html` — custom error page
- `robots.txt` — search engine directives
- `sitemap.xml` — site map
- `CNAME` — custom domain configuration
- `.nojekyll` — disables Jekyll for pure static serving

No external JavaScript, no dependencies, no backend.

---

## 2. Hosting and Domain

The site is hosted via **GitHub Pages** with:

- Custom domain: `ukoapp.com`
- DNS configured at PlanetHoster
- DNSSEC enabled
- HTTPS enforced (Let’s Encrypt)

This ensures full encryption and protection against DNS attacks  
(spoofing, hijacking, poisoning).

---

## 3. GitHub Pages Security (Summary)

The site follows strict security practices:

- HTTPS enforced
- DNSSEC enabled
- No sensitive files in the repository
- No external or untrusted JavaScript
- No executables hosted (binaries are served via AWS)
- `.nojekyll` for static serving
- Custom 404 page
- Minimal robots.txt (full crawl allowed)
- Clean and valid sitemap.xml

Attack surface: **zero**.

---

## 4. Repository Security (Summary)

The repository is configured to be minimal, locked down, and noise‑free.

### Disabled features
- Issues  
- Wiki  
- Discussions  
- Projects  
- Sponsorships  
- Template repository  
- GitHub Actions (disabled for maximum security)

### Branch protection (`main`)
- Pull Request required  
- Direct pushes blocked  
- Force pushes blocked  
- Branch deletion blocked  
- No bypass allowed  
- Only the owner can push  
- Automatic deletion of merged branches  
- Merge method: **Squash only**

Result:  
The `main` branch cannot be deleted, forced, overwritten, or bypassed.

---

## 5. Update Workflow

1. Create a branch  
   (`add-feature`, `update-content`, etc.)
2. Make changes  
3. Open a Pull Request  
4. Preview the GitHub Pages build  
5. Merge using **Squash**  
6. Branch is automatically deleted  

A clean, simple workflow with no unnecessary history.

---

## 6. Maintenance

- HTTPS certificate: automatic  
- DNS: rarely needs updates  
- Update `robots.txt` or `sitemap.xml` if the site evolves  
- Keep the repository clean (no unused files)

No server maintenance, no patches, no dependencies.

---

## 7. Purpose of This Repository

This repository is used exclusively to:

- host the UKOAPP landing website  
- maintain a clean and secure web presence  
- provide a stable, risk‑free static site  

All application logic (executables, backend, APIs) is hosted elsewhere  
(AWS S3 + CloudFront + Signed URLs).

---

## 8. Product Ownership

**UKOAPP is a product by Creacluster.**  
This repository contains only the public landing page.

---

## 9. Contact

For any inquiry regarding UKOAPP:  
**head-ukoapp@creacluster.com**
