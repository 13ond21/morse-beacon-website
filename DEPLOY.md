# Deploy Morse Beacon website to GitHub Pages

Play Console requires a live privacy policy URL before you can publish.

## Steps

1. Log in to GitHub and create a new **public** repository named `morse-beacon-website`
2. Do **not** initialise with README (you already have files)
3. Run from this folder:

```powershell
cd C:\Users\corey\morse_beacon\website
git init
git add .
git commit -m "Morse Beacon website v1.1"
git branch -M main
git remote add origin https://github.com/13ond21/morse-beacon-website.git
git push -u origin main
```

4. GitHub → repo **Settings** → **Pages**
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