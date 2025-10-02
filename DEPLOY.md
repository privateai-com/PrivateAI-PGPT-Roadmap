# Deployment Guide - GitHub Pages

## 🚀 Quick Deployment Steps

### Step 1: Initialize Git Repository

```bash
cd /Users/alex/Desktop/PrivateAI_PGPT_Roadmap

# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: PrivateAI $PGPT Ecosystem Roadmap"
```

### Step 2: Create GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository named: `PrivateAI-PGPT-Roadmap` (or your preferred name)
3. **Do NOT** initialize with README, .gitignore, or license (we already have these)
4. Click "Create repository"

### Step 3: Push to GitHub

```bash
# Add GitHub remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/PrivateAI-PGPT-Roadmap.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top right)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**

### Step 5: Wait for Deployment

- GitHub will build your site (takes 1-2 minutes)
- Your site will be available at: `https://YOUR_USERNAME.github.io/PrivateAI-PGPT-Roadmap/`
- You'll see a green checkmark when it's ready

---

## 🎨 Optional: Custom Domain

If you want to use a custom domain (e.g., `roadmap.privateai.com`):

### Step 1: Add CNAME File

```bash
echo "roadmap.privateai.com" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

### Step 2: Configure DNS

Add these DNS records to your domain:

**For subdomain (roadmap.privateai.com):**
```
Type: CNAME
Name: roadmap
Value: YOUR_USERNAME.github.io
```

**For apex domain (privateai.com):**
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

### Step 3: Enable in GitHub Settings

1. Go to Settings → Pages
2. Enter your custom domain: `roadmap.privateai.com`
3. Click Save
4. Wait for DNS check (can take up to 24 hours)
5. Enable "Enforce HTTPS" once DNS is verified

---

## 📊 Verify Deployment

Once deployed, check:

- ✅ Homepage loads: `https://YOUR_USERNAME.github.io/PrivateAI-PGPT-Roadmap/`
- ✅ Navigation works between pages
- ✅ All product pages load correctly
- ✅ Images and styling appear (if any)
- ✅ Mobile responsive design works

---

## 🔧 Troubleshooting

### Site Not Loading?

1. Check GitHub Actions tab for build errors
2. Verify GitHub Pages is enabled in Settings
3. Wait 5-10 minutes for initial deployment
4. Clear browser cache and try again

### 404 Errors?

1. Ensure all `.md` files are in root directory
2. Check that links use relative paths (e.g., `the-thing.md` not `/the-thing.md`)
3. Verify `_config.yml` is in root directory

### Styling Not Working?

1. Check `_config.yml` theme is set correctly
2. Verify Jekyll is building (check Actions tab)
3. Try adding `theme: jekyll-theme-cayman` to `_config.yml`

### Custom Domain Not Working?

1. Verify DNS records are correct
2. Wait 24-48 hours for DNS propagation
3. Check CNAME file is in root directory
4. Ensure custom domain is set in GitHub Settings

---

## 🎯 Post-Deployment Checklist

- [ ] Site is live and accessible
- [ ] All pages load correctly
- [ ] Navigation works between pages
- [ ] Mobile responsive design verified
- [ ] Share link with team
- [ ] Add to PrivateAI website
- [ ] Announce to community
- [ ] Monitor analytics (if configured)

---

## 📝 Making Updates

To update the roadmap after deployment:

```bash
# Make your changes to .md files

# Commit changes
git add .
git commit -m "Update: [describe your changes]"

# Push to GitHub
git push

# GitHub Pages will automatically rebuild (1-2 minutes)
```

---

## 🔗 Useful Links

- **GitHub Pages Docs**: https://docs.github.com/en/pages
- **Jekyll Themes**: https://pages.github.com/themes/
- **Custom Domains**: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

---

**Ready to deploy? Run the commands in Step 1 to get started!**
