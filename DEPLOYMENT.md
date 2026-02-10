# GitHub Pages Deployment Setup Guide

## 🎯 Quick Start - Enable Deployment

Your Pantra website is ready to deploy! Just follow these simple steps:

### Step 1: Merge Your Changes to Main Branch

**IMPORTANT:** GitHub Pages only deploys from the `main` branch for security.

1. **Merge the Pull Request**
   - Go to: https://github.com/gatherdevops-code/Pantra-site/pulls
   - Find and merge the PR for the support page
   - Or manually merge using: `git checkout main && git merge copilot/add-support-page-to-pantra && git push`

### Step 2: Configure GitHub Pages

1. **Go to repository Settings**
   - Navigate to: https://github.com/gatherdevops-code/Pantra-site/settings/pages
   - Or: Click "Settings" tab → Scroll down to "Pages" in the left sidebar

2. **Configure the Source**
   - Under "Build and deployment" section
   - For **Source**, select: **GitHub Actions** (NOT "Deploy from a branch")
   - The page should show: "Your site is ready to be deployed from the GitHub Actions workflow"

3. **Save**
   - Changes are automatically saved
   - The workflow will deploy automatically when you push to `main`

### Step 3: Verify Deployment

After merging to main and configuring GitHub Pages:

1. **Check the Actions tab**
   - Go to: https://github.com/gatherdevops-code/Pantra-site/actions
   - You should see "Deploy to GitHub Pages" workflow running
   - Wait for the green checkmark (usually 1-2 minutes)

2. **Access your site**
   - Your site will be live at: https://gatherdevops-code.github.io/Pantra-site/
   - It may take 1-2 minutes for the first deployment to complete

## 🔄 How Deployment Works

### Automatic Deployment
- **Triggers**: Every push to the `main` branch ONLY
- **Process**: GitHub Actions automatically builds and deploys
- **Duration**: Usually completes in 1-2 minutes
- **Branch Protection**: Feature branches cannot deploy (security measure)

### Manual Deployment
If you need to deploy manually:
1. Go to: https://github.com/gatherdevops-code/Pantra-site/actions
2. Click "Deploy to GitHub Pages" workflow
3. Click "Run workflow" button
4. **Select `main` branch** (other branches won't work due to environment protection)
5. Click "Run workflow"

## 🌐 Custom Domain (Optional)

If you want to use a custom domain (e.g., www.pantra.com):

### Step 1: Add Custom Domain in GitHub
1. Go to: https://github.com/gatherdevops-code/Pantra-site/settings/pages
2. Under "Custom domain", enter your domain
3. Click "Save"

### Step 2: Create CNAME File
Create a file named `CNAME` in the repository root containing your domain:
```
www.pantra.com
```

### Step 3: Configure DNS
At your domain provider (e.g., GoDaddy, Namecheap, Cloudflare):

**For apex domain (pantra.com):**
Add these A records:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**For www subdomain (www.pantra.com):**
Add a CNAME record pointing to: `gatherdevops-code.github.io`

### Step 4: Enable HTTPS (Recommended)
1. After DNS propagates (can take 24-48 hours)
2. Go to GitHub Pages settings
3. Check "Enforce HTTPS"

## 📝 What's Included

The deployment setup includes:

- ✅ **Automated workflow** - Deploys automatically on push
- ✅ **Manual trigger option** - Can deploy on-demand
- ✅ **`.nojekyll` file** - Optimizes deployment speed
- ✅ **Proper permissions** - Configured for GitHub Pages deployment
- ✅ **Concurrency control** - Prevents deployment conflicts

## 🐛 Troubleshooting

### "Branch is not allowed to deploy to github-pages"
- **Error**: `Branch "copilot/add-support-page-to-pantra" is not allowed to deploy to github-pages due to environment protection rules`
- **Cause**: GitHub Pages only allows deployment from the `main` branch for security
- **Solution**: 
  1. Merge your feature branch to `main` first
  2. The workflow will automatically deploy from `main`
  3. Never try to deploy directly from feature branches

### Workflow shows "action_required"
- **Cause**: GitHub Pages not configured yet
- **Solution**: Follow Step 2 above to enable GitHub Pages with "GitHub Actions" source

### Site not updating after push
- **Check**: Actions tab to see if workflow completed successfully
- **Check**: Pages settings to ensure source is "GitHub Actions"
- **Check**: You pushed to the `main` branch (not a feature branch)
- **Try**: Manually trigger the workflow from the `main` branch

### 404 Page Not Found
- **Check**: Site URL includes repository name: `/Pantra-site/`
- **Check**: Custom domain DNS settings if using custom domain
- **Wait**: First deployment can take a few minutes

## 📞 Support

If you encounter issues:
1. Check the Actions tab for workflow logs
2. Verify GitHub Pages settings
3. Contact gatherdevops@gmail.com for support

---

**🎉 That's it! Your Pantra marketing site is ready to go live!**
