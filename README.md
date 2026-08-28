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

The domain **ukoapp.com** uses a clean three‑layer architecture:

**Registrar — PlanetHoster**
PlanetHoster is used exclusively as the domain registrar.  
It does **not** host the website and does **not** manage SSL certificates.

**DNS — Cloudflare**
Cloudflare is the authoritative DNS provider for the domain.  
Configuration includes:
- DNSSEC enabled  
- Proxy mode (reverse‑proxy)  
- Security filtering  
- Apex domain pointing to GitHub Pages IPs  
- `www` subdomain pointing to `ukoapp.github.io`  
- SSL mode set to **Full** during GitHub Pages certificate provisioning  
- Can be switched to **Full (strict)** once GitHub’s Let’s Encrypt certificate is active

**Hosting — GitHub Pages**
The static site is hosted on GitHub Pages, which provides:
- Automatic HTTPS via **Let’s Encrypt**  
- Certificate renewal every ~90 days  
- Secure static hosting with no backend  
- Custom domain support (`ukoapp.com` and `www.ukoapp.com`)

This architecture ensures end‑to‑end encryption, automatic SSL renewal, and strong protection against DNS‑level attacks (spoofing, hijacking, 

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

UKOAPP is a product by **Creacluster**, currently operating as an informal
association (“association de fait”).  
Creacluster serves as the public brand identity, and may later transition to a
formal business structure (auto‑entreprise) while keeping the same name.

This repository contains only the public landing page.

---

## 9. Contact

For any inquiry regarding UKOAPP:

**head-ukoapp@creacluster.com**  
*(temporary contact address — will be replaced by a dedicated **@ukoapp.com**
address for production, Stripe verification, and long‑term branding)*.
