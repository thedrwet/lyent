
# ⚠️ ACTION REQUIRED: Enable GitHub Pages Deployment

## The Problem
Your deployment workflow exists and is configured correctly, but GitHub Pages is not enabled for this repository. This is why deployments are failing with:
```
Get Pages site failed. Please verify that the repository has Pages enabled
```

## The Solution (Takes 2 Minutes)

### Step 1: Go to Repository Settings
Click this link to go directly to your repository settings:
**https://github.com/thedrwet/lyent/settings/pages**

Or navigate manually:
1. Go to https://github.com/thedrwet/lyent
2. Click the **Settings** tab (⚙️ gear icon at the top)
3. In the left sidebar, scroll down and click **Pages**

### Step 2: Enable GitHub Actions as Source
In the Pages settings page:

1. Look for the **"Build and deployment"** section
2. Under **"Source"**, you'll see a dropdown menu
3. Click the dropdown and select **"GitHub Actions"**
4. The page will automatically save

You should see a message like:
> "Your site is being built from the GitHub Actions workflow"

### Step 3: Trigger Deployment
Now that Pages is enabled, trigger a deployment:

**Option A - Push any change:**
```bash
git commit --allow-empty -m "Trigger deployment"
git push origin main
```

**Option B - Manual workflow trigger:**
1. Go to https://github.com/thedrwet/lyent/actions
2. Click "Deploy static content to Pages"
3. Click "Run workflow" → Select "main" → Click "Run workflow"

### Step 4: Watch It Deploy
1. Go to https://github.com/thedrwet/lyent/actions
2. You should see "Deploy static content to Pages" running
3. Wait for the green checkmark ✅
4. Your site will be live at: **https://thedrwet.github.io/lyent/**

## That's It!
After completing Step 2, your site will automatically deploy whenever you push to the `main` branch.

---

## Why Can't This Be Automated?
GitHub requires the repository owner to manually enable Pages for security reasons. This setting cannot be changed via GitHub Actions, API, or command line tools. It's a one-time manual step that protects your repository.

## Need Help?
See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed troubleshooting and more information.
