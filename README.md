# enscribe-app-pages

Static support & privacy pages for Enscribe-published apps.

Hosted with **GitHub Pages** (no Node, no build step).

## Local preview

Open `index.html` in a browser, or:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## Enable GitHub Pages

1. Make the repo **public** (required for free Pages), or use GitHub Pro for private Pages.
2. Repo → **Settings** → **Pages**
3. Source: **Deploy from a branch**
4. Branch: `main` / folder: `/ (root)`
5. Save

Site URL will be:

`https://evanl01.github.io/enscribe-app-pages/`

Custom domain: `https://dev.enscribe.online`

### App Store Connect URLs

- Support (per app): `https://dev.enscribe.online/crossword-traveller/`
- Privacy (company-wide): `https://dev.enscribe.online/privacy.html`

### Custom domain (`dev.enscribe.online`)

1. Repo has a root `CNAME` file with `dev.enscribe.online`.
2. GitHub → **Settings** → **Pages** → Custom domain: `dev.enscribe.online` → Save → enable **Enforce HTTPS** once DNS checks pass.
3. Cloudflare → DNS → Add record:
   - Type: **CNAME**
   - Name: `dev`
   - Target: `evanl01.github.io`
   - Proxy: **DNS only** (grey cloud) until HTTPS works; you can turn proxy on later with SSL mode **Full**.
4. Wait a few minutes for DNS, then confirm `https://dev.enscribe.online` loads.
## Add another app

Create a folder with a support page:

```
other-app/
  index.html      # support (how to use / contact)
```

Link it from the root `index.html`. Point App Store privacy URLs at the shared `/privacy.html`.
