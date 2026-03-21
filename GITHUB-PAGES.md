# Put your site on GitHub Pages

Your HTML/CSS lives in **`website/`**. This repo includes a workflow that deploys **only that folder** so your site opens at:

**`https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`**

(no `/website/` in the URL)

---

## 1. Put the project on GitHub

1. Create a **new repository** on GitHub (empty, no README required).
2. On your PC, in this project folder, run in **PowerShell** or **Git Bash**:

```bash
git init
git add .
git commit -m "Initial commit — Mwinsi Nkosi site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

Replace `YOUR_USERNAME` and `YOUR_REPO_NAME`.

---

## 2. Turn on GitHub Pages (GitHub Actions)

1. On GitHub: open the repo → **Settings** → **Pages** (left sidebar).
2. Under **Build and deployment** → **Source**, choose **GitHub Actions** (not “Deploy from a branch”).
3. Go to **Actions** tab — the **Deploy GitHub Pages** workflow should run from your push. If it failed, open it and read the log.
4. When it’s green, refresh **Settings → Pages** — you’ll see **Your site is live at** `https://….github.io/…/`

First deploy can take **1–2 minutes**.

---

## 3. If your default branch is not `main`

Edit `.github/workflows/github-pages.yml` and change `branches: - main` to your branch name (e.g. `master`).

---

## 4. FormSubmit `thank-you.html` (optional)

After the site is live, in `website/index.html` uncomment/add:

```html
<input type="hidden" name="_next" value="https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/thank-you.html" />
```

Use your **exact** Pages URL (HTTPS).

---

## 5. Updating the site

Commit and push changes to `main` — the workflow redeploys automatically.
