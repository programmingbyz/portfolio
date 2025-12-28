# 🚀 Quick Start Guide

Get your portfolio live in 10 minutes!

## ⚡ Super Fast Deployment

### Step 1: Customize Your Info (5 minutes)

Open `index.html` and replace these key items:

1. **Line 6**: Update page title
2. **Line 35**: Your name in hero section
3. **Line 36**: Your subtitle/tagline
4. **Lines 70-75**: Your biography
5. **Lines 162-167**: Your contact information
6. **Lines 180-189**: Your social media URLs

### Step 2: Add Your Image

Replace the image path in `index.html`:
- Currently: `assets/images/0dd46d5a-a170-4102-a67e-7d9ffbd2ac73.jpeg`
- With: Your own image (add to `assets/images/` folder)

### Step 3: Deploy to GitHub (3 minutes)

```bash
# In your portfolio folder, run:

# If git is already initialized (check with: git status)
git add .
git commit -m "Customize portfolio with my information"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git branch -M main
git push -u origin main

# If git is NOT initialized:
git init
git add .
git commit -m "Initial commit: My portfolio website"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages (2 minutes)

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Source: **main** branch, **/ (root)** folder
4. Click **Save**
5. Wait 1-2 minutes

### Step 5: View Your Live Site! 🎉

Visit: `https://YOUR-USERNAME.github.io`

---

## 📝 What to Customize Later

For a complete customization, check these files:

- **CUSTOMIZATION-GUIDE.md** - Detailed personalization instructions
- **DEPLOYMENT-GUIDE.md** - Complete deployment documentation
- **README.md** - Full project documentation

---

## 🎨 Quick Color Change

Want to change colors quickly? Edit `assets/styles/style.css` (lines 12-17):

```css
:root {
    --primary-color: #2c3e50;     /* Change this */
    --secondary-color: #3498db;   /* And this */
    --accent-color: #e74c3c;      /* And this */
}
```

---

## 🖼️ Quick Image Tips

- **Hero background**: 1920x1080px (landscape)
- **About photo**: 800x800px (square/portrait)
- **Portfolio items**: 1200x800px (landscape)
- **Compress images**: Use [TinyPNG](https://tinypng.com)

---

## ❓ Quick Troubleshooting

**Assets not loading?**
- Check all paths in HTML are relative (no leading `/`)

**Changes not showing?**
- Clear browser cache (Ctrl+F5)
- Wait 1-2 minutes after pushing to GitHub

**Can't push to GitHub?**
- Make sure repository name is `YOUR-USERNAME.github.io`
- Check repository is set to **Public**

---

## 🎯 Essential Files

```
portfolio/
├── index.html              # Main HTML (customize this!)
├── assets/
│   ├── styles/style.css   # CSS styling
│   ├── js/script.js       # JavaScript interactions
│   └── images/            # Your photos here
```

---

## 🔗 Useful Links

- **Font Awesome Icons**: [fontawesome.com/icons](https://fontawesome.com/icons)
- **Google Fonts**: [fonts.google.com](https://fonts.google.com)
- **Color Picker**: [coolors.co](https://coolors.co)
- **Image Compression**: [tinypng.com](https://tinypng.com)

---

That's it! You're live! 🚀✨

For detailed customization, see the other guide files.

