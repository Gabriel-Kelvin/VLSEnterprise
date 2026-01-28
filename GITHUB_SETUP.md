# GitHub Setup & GitHub Pages Deployment Guide

Follow these steps to upload your JLS Enterprise landing page to GitHub and host it with GitHub Pages.

## Prerequisites

1. **Git installed** on your computer ([Download Git](https://git-scm.com/downloads))
2. **GitHub account** (you already have one: Gabriel-Kelvin)
3. **GitHub repository** created: `https://github.com/Gabriel-Kelvin/VLSEnterprise.git`

## Step 1: Initialize Git Repository (if not already done)

Open PowerShell or Command Prompt in your project directory and run:

```bash
cd "d:\CHRIST\JLS Enterprice"
git init
```

## Step 2: Add All Files to Git

```bash
git add index.html
git add styles.css
git add script.js
```

Or add all files at once:
```bash
git add .
```

## Step 3: Create Initial Commit

```bash
git commit -m "Initial commit: JLS Enterprise landing page"
```

## Step 4: Add Remote Repository

```bash
git remote add origin https://github.com/Gabriel-Kelvin/VLSEnterprise.git
```

## Step 5: Rename Branch to Main (if needed)

```bash
git branch -M main
```

## Step 6: Push to GitHub

```bash
git push -u origin main
```

**Note:** You'll be prompted to enter your GitHub username and password (or personal access token).

### If you get authentication errors:

1. **Use a Personal Access Token** instead of password:
   - Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Generate new token with `repo` permissions
   - Use this token as your password when pushing

2. **Or use SSH** (if you have SSH keys set up):
   ```bash
   git remote set-url origin git@github.com:Gabriel-Kelvin/VLSEnterprise.git
   git push -u origin main
   ```

## Step 7: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/Gabriel-Kelvin/VLSEnterprise`
2. Click on **Settings** (top menu)
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select:
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Click **Save**

## Step 8: Access Your Live Site

After enabling GitHub Pages, your site will be available at:
```
https://gabriel-kelvin.github.io/VLSEnterprise/
```

**Note:** It may take a few minutes (up to 10 minutes) for the site to be available after first deployment.

## Future Updates

Whenever you make changes to your files:

```bash
git add .
git commit -m "Description of your changes"
git push origin main
```

GitHub Pages will automatically rebuild and update your site within a few minutes.

## Troubleshooting

### If files don't appear on GitHub:
- Make sure you've committed the files: `git status`
- Check that you've pushed: `git push origin main`

### If GitHub Pages shows 404:
- Wait 5-10 minutes after enabling Pages
- Check that `index.html` is in the root directory
- Verify the branch is set to `main` in Pages settings

### If you need to change the repository name:
- The GitHub Pages URL will be: `https://gabriel-kelvin.github.io/[repository-name]/`
- Make sure the repository name matches what you want in the URL

## Files Included

Your repository contains:
- `index.html` - Main HTML file
- `styles.css` - All styling
- `script.js` - JavaScript functionality

All files are ready for GitHub Pages hosting!
