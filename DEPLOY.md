# Deploy Morse Beacon website to GitHub Pages

Play Console requires a live privacy policy URL before you can publish.

## Step 0 — Create the empty repo on GitHub (required first)

`git push` fails with **Repository not found** until this exists.

1. Open **https://github.com/new**
2. Repository name: `morse-beacon-website`
3. Visibility: **Public**
4. **Do not** tick “Add a README”, “Add .gitignore”, or “Choose a license”
5. Click **Create repository**

You should land on an empty repo page. Then push from your PC (Step 1).

## Step 1 — Push from your PC

If you already ran `git init` and committed, you only need:

```powershell
cd C:\Users\corey\morse_beacon\website
git push -u origin main
```

If `remote origin already exists` but push still fails, the repo was not created on GitHub yet — do Step 0.

**First-time setup** (only if you have not committed yet):

```powershell
cd C:\Users\corey\morse_beacon\website
git init
git add .
git commit -m "Morse Beacon website v1.1"
git branch -M main
git remote add origin https://github.com/13ond21/morse-beacon-website.git
git push -u origin main
```

If `git remote add` says origin already exists:

```powershell
git remote set-url origin https://github.com/13ond21/morse-beacon-website.git
git push -u origin main
```

## Step 2 — Enable GitHub Pages

1. GitHub → repo **Settings** → **Pages**
5. Source: **Deploy from a branch** → Branch: `main` → Folder: `/ (root)` → Save
6. Wait 1–2 minutes, then verify:
   - https://13ond21.github.io/morse-beacon-website/
   - https://13ond21.github.io/morse-beacon-website/privacy.html

## Update later

```powershell
git add .
git commit -m "Update website"
git push
```