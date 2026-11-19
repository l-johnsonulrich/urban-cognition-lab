# Urban Cognition Lab website

Plain HTML/CSS site (no build step), converted from the old Weebly export.
Hosted on GitHub Pages at https://lilyjohnsonulrich.com

## Files
- `index.html`, `people.html`, `publications.html`, `dei.html`, `photos.html`, `in-the-news.html`, `artscience.html` – the pages
- `css/style.css` – all styling (colors/fonts are at the top)
- `images/` – web-optimized photos
- `files/` – downloadable PDF/DOCX
- `CNAME` – tells GitHub Pages to use lilyjohnsonulrich.com

To edit text, open the .html file on GitHub, click the pencil icon, change the text, and commit. The site updates in ~1 minute.
The menu and footer are repeated on every page, so update all 7 files if you change them.

## 1. Put the site on GitHub
1. Sign in at github.com → **+** (top right) → **New repository**.
2. Name it (e.g. `lab-website`), set it to **Public**, click **Create repository**.
3. On the new repo page click **uploading an existing file**.
4. Unzip the site folder on your computer, open it, select **everything inside it** (including the `css`, `images`, `files` folders and `CNAME`) and drag it into the browser. Click **Commit changes**.
   - `.nojekyll` is a hidden file; if it doesn't upload that's fine.
5. Repo **Settings → Pages**. Under "Build and deployment": Source = **Deploy from a branch**, Branch = **main**, folder = **/(root)** → **Save**.
6. Under "Custom domain" type `lilyjohnsonulrich.com` → **Save** (the CNAME file usually fills this in already).

## 2. Point the Cloudflare domain at GitHub
Cloudflare dashboard → click `lilyjohnsonulrich.com` → **DNS → Records**. Delete any existing A/AAAA/CNAME records for `@` and `www` (e.g. parking records), then add:

| Type  | Name | Content                  | Proxy status |
|-------|------|--------------------------|--------------|
| A     | @    | 185.199.108.153          | DNS only (grey cloud) |
| A     | @    | 185.199.109.153          | DNS only |
| A     | @    | 185.199.110.153          | DNS only |
| A     | @    | 185.199.111.153          | DNS only |
| CNAME | www  | YOUR-GITHUB-USERNAME.github.io | DNS only |

Click the orange cloud to turn it grey ("DNS only") so GitHub can issue the HTTPS certificate.

## 3. Turn on HTTPS
Wait 10 minutes to a few hours for DNS. Back in **Settings → Pages**, the domain check should turn green; then tick **Enforce HTTPS**.
(Optional, after HTTPS works: you can switch the Cloudflare records to Proxied, but then set Cloudflare **SSL/TLS** mode to **Full**, or you'll get redirect loops.)

## 4. Recommended
- Verify the domain: GitHub profile **Settings → Pages → Add a domain** and add the TXT record it gives you in Cloudflare. This prevents domain takeovers.
- Once the new site is live, cancel/unpublish the Weebly site.
