# Deployment Guide - GitHub Pages

## Quick Start

This website is configured to automatically deploy to GitHub Pages when you push to the `main` branch.

## Step-by-Step Setup

### 1. Push to GitHub

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Commit your changes
git commit -m "Initial commit: Personal website"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git push -u origin main
```

### 2. Enable GitHub Pages

1. Go to your GitHub repository
2. Click on **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select **GitHub Actions**
5. The deployment will start automatically

### 3. Access Your Website

After the deployment completes (usually 1-2 minutes), your website will be available at:

```
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
```

## What's Been Set Up

- ✅ `.nojekyll` file - Prevents GitHub from processing the site with Jekyll
- ✅ `.github/workflows/deploy.yml` - Automated deployment workflow
- ✅ Static HTML/CSS/JS files - Your complete website

## Updating Your Website

To update your website after the initial deployment:

```bash
# Make your changes to index.html, styles.css, etc.

# Commit and push
git add .
git commit -m "Update website content"
git push origin main
```

The GitHub Action will automatically redeploy your site with the changes.

## Troubleshooting

### Deployment Failed
- Check the **Actions** tab in your GitHub repository
- Review the error logs
- Ensure GitHub Pages is enabled in repository settings

### 404 Error
- Verify the repository name in your URL
- Check that `index.html` exists in the root directory
- Wait a few minutes for DNS propagation

### Images Not Loading
- Ensure image files are committed to the repository
- Check file names match exactly (case-sensitive)
- Use relative paths (e.g., `./image.jpg` not `/image.jpg`)

## Custom Domain (Optional)

To use a custom domain:

1. Add a `CNAME` file to the repository root with your domain
2. Configure DNS records with your domain provider
3. Update GitHub Pages settings to use your custom domain

## Files Overview

```
personal-website-2/
├── index.html              # Main website file
├── styles.css              # All styling
├── IMG_1481.jpg           # Profile picture (old)
├── Untitled design (6).png # Profile picture (current)
├── .nojekyll              # GitHub Pages config
├── .github/
│   └── workflows/
│       └── deploy.yml     # Auto-deployment workflow
├── package.json           # Project metadata
└── README.md             # Project documentation
```
