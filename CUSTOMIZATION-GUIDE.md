# Portfolio Customization Guide

This guide will help you personalize your portfolio website with your own information.

## 🎯 Quick Customization Checklist

### 1. Personal Information (index.html)

#### Hero Section
- [ ] Update the name in the hero title (currently "Fahim Shariar")
- [ ] Modify the subtitle/tagline
- [ ] Adjust photography categories (Fashion, Lifestyle, Food) if needed

#### About Section
- [ ] Replace the biography text with your own story
- [ ] Update university name (currently "North South University")
- [ ] Modify skill items to match your expertise
- [ ] Replace the about image with your photo

#### Contact Section
Replace these placeholder values:
- [ ] Email: `fahim.shariar@example.com`
- [ ] Phone: `+880 1234 567 890`
- [ ] Location: `Dhaka, Bangladesh`

#### Social Media Links
Update URLs in both contact section and footer:
- [ ] Instagram: `https://instagram.com/YOUR_USERNAME`
- [ ] Twitter: `https://twitter.com/YOUR_USERNAME`
- [ ] LinkedIn: `https://linkedin.com/in/YOUR_USERNAME`
- [ ] GitHub: `https://github.com/YOUR_USERNAME`

### 2. Images

#### Add Your Own Photos
1. Place your images in `assets/images/` folder
2. Update image sources in `index.html`:
   - Hero background (line ~50)
   - About section image (line ~100)
   - Portfolio items in Work section (lines ~135-200)

#### Recommended Image Sizes
- Hero background: 1920x1080px (landscape)
- About image: 800x800px (square or portrait)
- Portfolio items: 1200x800px (landscape)

### 3. Portfolio Items

#### Add New Work
Copy this template and paste it in the Work section:

```html
<div class="work-item" data-category="CATEGORY">
    <div class="work-image">
        <img src="assets/images/YOUR-IMAGE.jpg" alt="Description">
        <div class="work-overlay">
            <h3>Project Title</h3>
            <p>Project Category</p>
            <button class="view-btn"><i class="fas fa-eye"></i> View</button>
        </div>
    </div>
</div>
```

**Categories available:**
- `fashion` - Fashion photography
- `lifestyle` - Lifestyle photography  
- `food` - Food photography
- Add your own categories by updating filter buttons

### 4. Color Scheme (assets/styles/style.css)

#### Primary Colors
Edit the CSS variables at the top of `style.css`:

```css
:root {
    --primary-color: #2c3e50;      /* Main dark color */
    --secondary-color: #3498db;    /* Blue accent */
    --accent-color: #e74c3c;       /* Red accent */
    --text-color: #333;            /* Body text */
    --light-text: #777;            /* Secondary text */
}
```

#### Popular Color Combinations

**Professional Blue:**
```css
--primary-color: #1a1a2e;
--secondary-color: #16213e;
--accent-color: #0f3460;
```

**Creative Purple:**
```css
--primary-color: #2d1b69;
--secondary-color: #8e44ad;
--accent-color: #c39bd3;
```

**Modern Green:**
```css
--primary-color: #1e3a20;
--secondary-color: #27ae60;
--accent-color: #58d68d;
```

### 5. Typography

#### Change Fonts
Replace Google Fonts in `index.html` (line ~13):

Current fonts:
- Headings: Playfair Display
- Body: Poppins

Popular alternatives:
- **Elegant**: Cormorant Garamond + Raleway
- **Modern**: Montserrat + Open Sans
- **Tech**: Roboto Mono + Inter

Then update in `style.css`:
```css
body {
    font-family: 'YOUR-BODY-FONT', sans-serif;
}

.section-title, .hero-title {
    font-family: 'YOUR-HEADING-FONT', serif;
}
```

### 6. Add More Sections

#### Blog Section Template
```html
<section id="blog" class="blog">
    <div class="container">
        <h2 class="section-title">Latest Posts</h2>
        <!-- Add blog content here -->
    </div>
</section>
```

#### Testimonials Section Template
```html
<section id="testimonials" class="testimonials">
    <div class="container">
        <h2 class="section-title">What Clients Say</h2>
        <!-- Add testimonials here -->
    </div>
</section>
```

### 7. SEO Optimization

#### Update Meta Tags (index.html)
```html
<title>Your Name - Photographer & Developer</title>
<meta name="description" content="Your custom description here">
<meta name="keywords" content="photography, fashion, lifestyle, portfolio">
<meta name="author" content="Your Name">

<!-- Open Graph (for social media sharing) -->
<meta property="og:title" content="Your Name - Portfolio">
<meta property="og:description" content="Your description">
<meta property="og:image" content="URL to your image">
<meta property="og:url" content="Your website URL">
```

### 8. Contact Form

#### Connect to Email Service
The current form shows a success message but doesn't send emails. To make it functional:

**Option 1: FormSubmit.co (Free, No Backend)**
```html
<form action="https://formsubmit.co/your@email.com" method="POST">
    <!-- Your form fields -->
</form>
```

**Option 2: Formspree (Free tier available)**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <!-- Your form fields -->
</form>
```

**Option 3: Google Forms**
- Create a Google Form
- Embed it in your contact section

### 9. Analytics (Optional)

#### Add Google Analytics
Add before closing `</head>` tag:

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

### 10. Performance Tips

#### Image Optimization
- Use WebP format for better compression
- Compress images before uploading (use TinyPNG or similar)
- Add width/height attributes to img tags

#### Minify Files (Before deployment)
- Use online minifiers for CSS and JS
- Or use build tools like Parcel, Webpack

## 🚀 Testing Before Deployment

1. **Test Locally**: Open in multiple browsers
2. **Mobile Testing**: Use browser dev tools device mode
3. **Links**: Verify all links work
4. **Forms**: Test contact form submission
5. **Images**: Ensure all images load correctly
6. **Responsive**: Check on different screen sizes

## 📱 Mobile Optimization Checklist

- [ ] Text is readable without zooming
- [ ] Buttons are easily tappable (min 44x44px)
- [ ] Navigation menu works on mobile
- [ ] Images load properly
- [ ] No horizontal scrolling

## ✅ Pre-Deployment Checklist

- [ ] All placeholder text replaced
- [ ] All images updated
- [ ] Contact information updated
- [ ] Social media links updated
- [ ] Meta tags customized
- [ ] Tested on multiple devices
- [ ] Forms tested
- [ ] All links verified
- [ ] .gitignore configured
- [ ] README updated with your info

## 🆘 Need Help?

If you encounter issues:
1. Check browser console for errors (F12)
2. Validate HTML: https://validator.w3.org/
3. Validate CSS: https://jigsaw.w3.org/css-validator/
4. Check responsive design: Use browser DevTools

---

Happy customizing! 🎨✨

