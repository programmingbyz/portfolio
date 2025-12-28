# GitHub Pages Deployment Guide

Complete step-by-step guide to deploy your portfolio website on GitHub Pages.

## 📋 Prerequisites

- [ ] Git installed on your computer
- [ ] GitHub account created
- [ ] Portfolio customization completed (see CUSTOMIZATION-GUIDE.md)

## 🚀 Deployment Steps

### Method 1: Deploy to username.github.io (Recommended)

This will make your site available at `https://YOUR-USERNAME.github.io`

#### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **"+"** button (top right) → **"New repository"**
3. Name it exactly: `YOUR-USERNAME.github.io`
   - Example: If your username is `fahimshariar`, name it `fahimshariar.github.io`
4. **Important**: Make it **Public**
5. **Do NOT** initialize with README (your local repo already has one)
6. Click **"Create repository"**

#### Step 2: Push Your Code

Open Terminal/Command Prompt in your portfolio folder and run:

```bash
# Check if git is already initialized (you should see .git folder)
git status

# If already initialized, just add the remote
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git

# Or if not initialized:
git init
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git

# Stage all files
git add .

# Commit your changes
git commit -m "Initial commit: Portfolio website"

# Push to GitHub
git branch -M main
git push -u origin main
```

#### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **"Settings"** tab
3. Scroll down to **"Pages"** section (left sidebar)
4. Under **"Source"**:
   - Branch: Select `main`
   - Folder: Select `/ (root)`
5. Click **"Save"**
6. Wait 1-2 minutes for deployment

#### Step 4: Visit Your Site

Your site will be live at:
```
https://YOUR-USERNAME.github.io
```

---

### Method 2: Deploy to Custom Repository

This will make your site available at `https://YOUR-USERNAME.github.io/REPO-NAME`

#### Step 1: Create Repository

1. Go to GitHub → New repository
2. Name it anything you like (e.g., `portfolio`, `my-portfolio`)
3. Make it **Public**
4. Click **"Create repository"**

#### Step 2: Update Base URL (if needed)

If your repository name is NOT your username.github.io, you may need to update links:

In `index.html`, ensure all asset paths are relative:
```html
<!-- Good (relative paths) -->
<link rel="stylesheet" href="assets/styles/style.css">
<script src="assets/js/script.js"></script>

<!-- Avoid absolute paths like /assets/... -->
```

#### Step 3: Push Your Code

```bash
git init
git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git
git add .
git commit -m "Initial commit: Portfolio website"
git branch -M main
git push -u origin main
```

#### Step 4: Enable GitHub Pages

1. Repository → Settings → Pages
2. Source: `main` branch, `/ (root)` folder
3. Save

Your site will be at: `https://YOUR-USERNAME.github.io/REPO-NAME`

---

## 🔧 Common Issues & Solutions

### Issue 1: Assets Not Loading

**Problem**: CSS/JS/Images not loading after deployment

**Solution**: 
- Ensure all paths are relative (no leading `/`)
- Check file names match exactly (case-sensitive on Linux servers)

```html
<!-- ✅ Correct -->
<link rel="stylesheet" href="assets/styles/style.css">

<!-- ❌ Incorrect (may work locally but fail on GitHub Pages) -->
<link rel="stylesheet" href="/assets/styles/style.css">
```

### Issue 2: 404 Page Not Found

**Problem**: Site shows 404 error

**Solutions**:
1. Ensure repository is **Public**
2. Wait 2-3 minutes after enabling Pages
3. Check Pages settings: Source must be `main` branch
4. Verify `index.html` is in the root folder (not in a subfolder)

### Issue 3: Changes Not Updating

**Problem**: Made changes but site not updating

**Solutions**:
1. Clear browser cache (Ctrl+F5 or Cmd+Shift+R)
2. Check if changes are pushed to GitHub
3. Wait 1-2 minutes for GitHub Pages to rebuild
4. Check GitHub Actions tab for build status

### Issue 4: Images Too Large / Slow Loading

**Solution**:
1. Compress images before uploading:
   - Use [TinyPNG](https://tinypng.com/)
   - Or [Squoosh](https://squoosh.app/)
2. Convert to WebP format for better compression
3. Recommended max size: 500KB per image

### Issue 5: Permission Denied (Push Rejected)

**Solution**:
```bash
# If you get authentication errors, use Personal Access Token
# GitHub Settings → Developer Settings → Personal Access Tokens
# Generate new token with 'repo' permissions

# Use token as password when pushing
git push -u origin main
```

Or set up SSH keys:
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your_email@example.com"

# Add to GitHub: Settings → SSH Keys → New SSH Key
# Then use SSH URL instead:
git remote set-url origin git@github.com:YOUR-USERNAME/REPO-NAME.git
```

---

## 🎨 Custom Domain (Optional)

Want to use your own domain like `www.yourname.com`?

### Step 1: Buy Domain
- Purchase from: Namecheap, GoDaddy, Google Domains, etc.

### Step 2: Configure DNS

Add these DNS records at your domain registrar:

```
Type    Name    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
CNAME   www     YOUR-USERNAME.github.io
```

### Step 3: Update GitHub Pages

1. Go to repository Settings → Pages
2. Under "Custom domain", enter your domain
3. Click Save
4. Wait for DNS check to complete (can take 24-48 hours)
5. Enable "Enforce HTTPS" after DNS is verified

### Step 4: Add CNAME File

Create a file named `CNAME` (no extension) in your repository root:

```
www.yourname.com
```

Commit and push:
```bash
git add CNAME
git commit -m "Add custom domain"
git push
```

---

## 📊 Post-Deployment Checklist

After deployment, verify:

- [ ] Site loads at the correct URL
- [ ] All images display correctly
- [ ] Navigation links work
- [ ] Mobile responsive design works
- [ ] Contact form displays properly
- [ ] Social media links work
- [ ] All sections scroll smoothly
- [ ] No console errors (F12 → Console)

---

## 🔄 Updating Your Site

Whenever you make changes:

```bash
# Stage your changes
git add .

# Commit with a descriptive message
git commit -m "Update about section and add new photos"

# Push to GitHub
git push

# Wait 1-2 minutes for changes to appear
```

---

## 📈 Optional Enhancements

### Add Google Analytics

1. Create account at [Google Analytics](https://analytics.google.com/)
2. Get your Measurement ID
3. Add to `index.html` before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Add Favicon

1. Create/generate a favicon (16x16 and 32x32 px)
2. Place in root folder as `favicon.ico`
3. Add to `<head>`:

```html
<link rel="icon" type="image/x-icon" href="favicon.ico">
```

### Performance Optimization

**Before deploying**, consider:

1. **Minify CSS/JS**: Use online tools or build tools
2. **Compress images**: Reduce file sizes
3. **Enable caching**: GitHub Pages does this automatically
4. **Use CDN for libraries**: Keep Font Awesome on CDN

---

## 🆘 Need Help?

### Useful Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)
- [Custom Domain Help](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

### Check Build Status

1. Go to your repository on GitHub
2. Click **"Actions"** tab
3. Check if the latest workflow succeeded

### Test Locally First

Before pushing to GitHub:

```bash
# Start local server
python -m http.server 8000

# Or use Node.js
npx http-server

# Visit: http://localhost:8000
```

---

## ✅ Success!

If everything works:
- ✨ Your portfolio is now live on the internet!
- 🌍 Share your URL with friends and on social media
- 💼 Add it to your resume and LinkedIn
- 📧 Include it in your email signature

**Your live site**: `https://YOUR-USERNAME.github.io`

---

**Congratulations!** 🎉 You've successfully deployed your portfolio to GitHub Pages!

