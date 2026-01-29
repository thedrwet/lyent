# Lyent - Digital Solutions Provider

A professional services webpage showcasing cloud solutions, IT consulting, quality assurance & testing, and data analytics services.

## 🚀 Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the `main` branch.

**Live Site:** https://thedrwet.github.io/lyent/

### Deployment Process

The site uses GitHub Actions for continuous deployment:
- Push changes to the `main` branch
- GitHub Actions workflow (`.github/workflows/static.yml`) automatically deploys the site
- Changes are live within minutes

### Manual Deployment

You can also trigger a manual deployment:
1. Go to the [Actions tab](https://github.com/thedrwet/lyent/actions)
2. Select "Deploy static content to Pages"
3. Click "Run workflow"

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
