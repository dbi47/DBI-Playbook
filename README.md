# DBI-Playbook
# DBI New Hire Playbook
**Duisburg Business Innovation — Internal Onboarding Dashboard**

A practical, interactive guide for new hires to navigate their first weeks and months at DBI. Not the HR Manual — a living, human guide to how DBI actually works.

---

## 🚀 Deploy to Netlify via GitHub

### Step 1 — Push to GitHub

```bash
# In your terminal
git init
git add .
git commit -m "Initial DBI Playbook"
git remote add origin https://github.com/YOUR_USERNAME/dbi-playbook.git
git push -u origin main
```

### Step 2 — Create Netlify Site

1. Go to [app.netlify.com](https://app.netlify.com) and log in
2. Click **"Add new site"** → **"Import an existing project"**
3. Choose **GitHub** and select your `dbi-playbook` repository
4. Under **Build settings**, set:
   - Build command: *(leave blank)*
   - Publish directory: `.`
5. Click **"Deploy site"**

### Step 3 — Add Secrets for GitHub Actions (auto-deploy)

Go to your GitHub repo → **Settings → Secrets and variables → Actions** → **New repository secret**

| Secret name | Where to find it |
|---|---|
| `NETLIFY_AUTH_TOKEN` | Netlify → User Settings → Applications → Personal access tokens |
| `NETLIFY_SITE_ID` | Netlify → Site → Site configuration → Site ID |

Once set, every push to `main` will auto-deploy. Pull requests get a preview URL.

---

## 📁 File Structure

```
dbi-playbook/
├── index.html           ← The entire dashboard (single file)
├── netlify.toml         ← Netlify config (headers, redirects)
├── README.md            ← This file
└── .github/
    └── workflows/
        └── deploy.yml   ← GitHub Actions auto-deploy
```

---

## ✏️ How to Update Content

All content lives in `index.html`. Each section has a clearly marked comment:

```html
<!-- ── Welcome ── -->
<!-- ── Modules ── -->
<!-- ── Roadmap ── -->
<!-- ── Tools ── -->
<!-- ── Decisions ── -->
<!-- ── Checklist ── -->
<!-- ── Contacts ── -->
```

To add a new section:
1. Add a `<section id="your-id" class="section">` block in `<main>`
2. Add a `<button class="sidebar-link" onclick="showSection('your-id', this)">` in the sidebar

---

## 🎨 Colours

| Token | Hex | Usage |
|---|---|---|
| `--navy` | `#1A2B4A` | Headers, primary text, dark elements |
| `--teal` | `#0A7EA4` | Primary accent, links, active states |
| `--teal-lt` | `#E8F6FB` | Teal backgrounds, info boxes |
| `--gold` | `#E8A020` | Secondary accent, highlights |
| `--gold-lt` | `#FDF4E3` | Gold backgrounds, warning boxes |
| `--off-white` | `#F5F7FA` | Page background |

---

## 📬 Questions?

Contact the DBI HR Project team or your direct lead.
