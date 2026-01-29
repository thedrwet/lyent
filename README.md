# Lyent - Digital Solutions Provider

A professional services webpage showcasing cloud solutions, IT consulting, quality assurance & testing, and data analytics services.

---

## 🚨 TO DEPLOY THIS PROJECT

**→ [Click here for deployment instructions](ENABLE_DEPLOYMENT.md) ←**

Your deployment workflow is ready, but you need to **enable GitHub Pages** (takes 2 minutes).

---

## 🚀 Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the `main` branch.

**Live Site:** https://thedrwet.github.io/lyent/

### Initial Setup (Required)

**⚠️ If you're experiencing deployment issues, you need to enable GitHub Pages first!**

Quick setup:
1. Go to **Settings** → **Pages** 
2. Set **Source** to "GitHub Actions"
3. Save and push to `main` branch

📖 **[Read the complete deployment guide →](DEPLOYMENT.md)** for detailed step-by-step instructions and troubleshooting.

### Deployment Process

After initial setup, the site uses GitHub Actions for continuous deployment:
- Push changes to the `main` branch
- GitHub Actions workflow (`.github/workflows/static.yml`) automatically deploys the site
- Changes are live within minutes

### Manual Deployment

You can also trigger a manual deployment:
1. Go to the [Actions tab](https://github.com/thedrwet/lyent/actions)
2. Select "Deploy static content to Pages"
3. Click "Run workflow"

### Troubleshooting

**Deployment fails with "Get Pages site failed" error:**
- **Cause:** GitHub Pages is not enabled or not configured to use GitHub Actions
- **Solution:** Follow the [Initial Setup](#initial-setup-required) instructions above

**Deployment succeeds but site doesn't update:**
- Clear your browser cache
- Check that you're viewing the correct URL: https://thedrwet.github.io/lyent/
- Wait a few minutes for GitHub's CDN to update

## 📁 Project Structure

```
lyent/
├── index.html          # Main webpage
├── styles.css          # Stylesheet
├── README.md           # This file
└── .github/
    └── workflows/
        └── static.yml  # GitHub Pages deployment workflow
```

## 🎨 Features

- **Responsive Design:** Works on desktop, tablet, and mobile devices
- **Accessibility:** WCAG compliant with skip navigation, ARIA labels, and semantic HTML
- **Modern UI:** Gradient backgrounds, smooth animations, and hover effects
- **Service Sections:**
  - Cloud Solutions
  - IT Consulting
  - Quality Assurance & Testing
  - Data Analytics
  - Additional Services (Mobile, Cybersecurity, AI/ML, Web Dev, Infrastructure, Analytics)

## 🛠️ Local Development

To run the site locally:

```bash
# Clone the repository
git clone https://github.com/thedrwet/lyent.git
cd lyent

# Start a local server (any of these options):
python3 -m http.server 8080
# or
npx serve
# or
php -S localhost:8080

# Open http://localhost:8080 in your browser
```

## 📝 License

© 2026 Lyent. All rights reserved.
