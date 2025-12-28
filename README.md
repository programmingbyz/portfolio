# Fahim Shariar - Portfolio Website

A modern, interactive portfolio website showcasing photography work and computer science projects.

## 🌟 Features

- **Responsive Design**: Fully responsive layout that works on all devices
- **Interactive Elements**: Smooth animations, hover effects, and transitions
- **Portfolio Gallery**: Filterable gallery to showcase different categories of work
- **Contact Form**: Integrated contact form for easy communication
- **Modern UI**: Clean, professional design with beautiful typography
- **Fast Loading**: Optimized for performance with lazy loading images
- **GitHub Pages Ready**: Static HTML/CSS/JS optimized for GitHub Pages hosting

## 🎨 Sections

1. **Hero Section**: Eye-catching introduction with category highlights (Fashion, Lifestyle, Food)
2. **About Section**: Personal information about education and skills
3. **Work Section**: Filterable portfolio gallery showcasing photography work
4. **Contact Section**: Contact information and form for inquiries
5. **Footer**: Quick links and social media connections

## 🚀 Quick Start

### Local Development

1. Clone this repository:
```bash
git clone https://github.com/YOUR-USERNAME/portfolio.git
cd portfolio
```

2. Open `index.html` in your browser or use a local server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

3. Visit `http://localhost:8000` in your browser

### Deploying to GitHub Pages

1. Create a new repository on GitHub named `YOUR-USERNAME.github.io` or any name you prefer

2. Initialize git and push your code:
```bash
git init
git add .
git commit -m "Initial commit: Portfolio website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

3. Enable GitHub Pages:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Under "Source", select `main` branch
   - Click "Save"
   - Your site will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

## 📝 Customization

### Update Personal Information

1. **Contact Details**: Edit the contact section in `index.html` (lines with placeholder emails, phone numbers, etc.)
2. **About Section**: Update the biography and education information
3. **Social Media Links**: Replace placeholder URLs with your actual social media profiles
4. **Images**: Replace placeholder images with your own photos in the `assets/images/` folder

### Add More Portfolio Items

To add more portfolio items, duplicate a `.work-item` div in the Work section:

```html
<div class="work-item" data-category="YOUR-CATEGORY">
    <div class="work-image">
        <img src="assets/images/YOUR-IMAGE.jpg" alt="Description">
        <div class="work-overlay">
            <h3>Project Title</h3>
            <p>Category Name</p>
            <button class="view-btn"><i class="fas fa-eye"></i> View</button>
        </div>
    </div>
</div>
```

### Customize Colors

Edit the CSS variables in `assets/styles/style.css`:

```css
:root {
    --primary-color: #2c3e50;
    --secondary-color: #3498db;
    --accent-color: #e74c3c;
    /* ... other variables ... */
}
```

## 📁 File Structure

```
portfolio/
│
├── index.html              # Main HTML file
├── README.md              # This file
│
├── assets/
│   ├── images/            # Image assets
│   │   └── 0dd46d5a...jpeg
│   │
│   ├── styles/            # CSS files
│   │   └── style.css
│   │
│   └── js/                # JavaScript files
│       └── script.js
```

## 🛠️ Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with Flexbox and Grid
- **JavaScript (Vanilla)**: Interactive features and animations
- **Font Awesome**: Icon library
- **Google Fonts**: Poppins & Playfair Display

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Fahim Shariar**
- Photographer
- Computer Science & Engineering Student
- North South University

## 🤝 Contributing

Feel free to fork this project and customize it for your own use!

## 📧 Contact

For any questions or suggestions, please reach out through the contact form on the website.

---

**Note**: Remember to replace all placeholder content (email, phone, social media links, images) with your actual information before deploying!

Made with ❤️ by Fahim Shariar
