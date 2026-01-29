# Deployment Guide for Lyent

## Problem: "Cannot Deploy This Project"

If you're experiencing deployment issues, the most common cause is that **GitHub Pages is not enabled** or **not configured to use GitHub Actions** as the build source.

## Solution: Enable GitHub Pages with GitHub Actions

Follow these steps to fix the deployment issue:

### Step 1: Enable GitHub Pages

1. Navigate to your repository on GitHub: `https://github.com/thedrwet/lyent`
2. Click on **Settings** (gear icon in the top right)
3. In the left sidebar, scroll down and click on **Pages**

### Step 2: Configure Build Source

In the Pages settings:

1. Under **Build and deployment** section:
   - Find the **Source** dropdown menu
   - Select **GitHub Actions** (NOT "Deploy from a branch")
   
2. You should see a message: "GitHub Pages is configured to build from the GitHub Actions workflow"

3. No need to select a branch or folder - GitHub Actions will handle this

### Step 3: Verify the Configuration

After configuring, you should see:
- Source: GitHub Actions
- A note that your site will be published from the workflow

### Step 4: Trigger a Deployment

Option A - Push to main branch:
```bash
git add .
git commit -m "Trigger deployment"
git push origin main
```

Option B - Manual workflow trigger:
1. Go to the **Actions** tab in your repository
2. Click on "Deploy static content to Pages" workflow
3. Click "Run workflow" button
4. Select the `main` branch
5. Click "Run workflow"

### Step 5: Monitor Deployment

1. Go to the **Actions** tab
2. You should see the "Deploy static content to Pages" workflow running
3. Once complete (green checkmark), your site will be live at: `https://thedrwet.github.io/lyent/`

## Common Issues and Solutions

### Error: "Get Pages site failed. Please verify that the repository has Pages enabled"

**Cause:** GitHub Pages is not enabled or not configured to use GitHub Actions.

**Solution:** Follow steps 1-3 above to enable GitHub Pages with GitHub Actions as the source.

### Error: "pages build and deployment" workflow appears instead

**Cause:** GitHub Pages is set to "Deploy from a branch" instead of "GitHub Actions".

**Solution:** 
1. Go to Settings → Pages
2. Change Source to "GitHub Actions"
3. The old workflow will stop, and your `.github/workflows/static.yml` will take over

### Workflow runs but site doesn't update

**Possible causes:**
1. Browser cache - Try hard refresh (Ctrl+F5 or Cmd+Shift+R)
2. GitHub CDN propagation delay - Wait 5-10 minutes
3. Wrong URL - Ensure you're visiting `https://thedrwet.github.io/lyent/` (not just `github.io/lyent`)

### Permission errors in workflow

**Cause:** Workflow doesn't have proper permissions.

**Solution:** Our workflow already includes the correct permissions:
```yaml
permissions:
  contents: read
  pages: write
  id-token: write
```

If you modified the workflow, ensure these permissions are present.

## Verification

Once deployment succeeds, you can verify:

1. **Actions tab**: Workflow shows green checkmark
2. **Live site**: Visit `https://thedrwet.github.io/lyent/`
3. **Pages settings**: Shows "Your site is live at https://thedrwet.github.io/lyent/"

## Technical Details

### How It Works

1. When you push to `main` or trigger manually, the workflow runs
2. The workflow:
   - Checks out your code
   - Configures GitHub Pages
   - Uploads the repository contents as an artifact
   - Deploys the artifact to GitHub Pages
3. GitHub serves your site from the Pages environment

### Workflow File

The deployment is configured in `.github/workflows/static.yml`:
- Triggers on push to `main` branch
- Can be manually triggered
- Uses official GitHub Actions for Pages deployment
- Deploys the entire repository root (where `index.html` is located)

## Need More Help?

If you continue to experience issues after following this guide:

1. Check the workflow logs in the Actions tab for specific error messages
2. Verify your repository is public (or you have GitHub Pages enabled for private repos)
3. Ensure the `main` branch exists and contains `index.html` and `styles.css`
4. Check that Actions are enabled for your repository (Settings → Actions → General)
