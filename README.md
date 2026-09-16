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

### App Store Connect URLs

- Support (per app): `https://evanl01.github.io/enscribe-app-pages/crossword-traveller/`
- Privacy (company-wide): `https://evanl01.github.io/enscribe-app-pages/privacy.html`

### Custom domain (optional later)

1. Add a `CNAME` file in the repo root with e.g. `apps.enscribe.online`
2. Point DNS CNAME `apps` → `evanl01.github.io`
3. Enable HTTPS in Pages settings

## Add another app

Create a folder with a support page:

```
other-app/
  index.html      # support (how to use / contact)
```

Link it from the root `index.html`. Point App Store privacy URLs at the shared `/privacy.html`.
