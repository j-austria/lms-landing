# LownDesk Landing Page

Modern, responsive landing page for the LownDesk Lending Management System.

## 📁 Project Structure

```
lms-landing/
├── index.html          # Homepage
├── features.html       # Features page
├── pricing.html        # Pricing page
├── css/
│   └── style.css      # Main stylesheet
├── js/
│   └── main.js        # JavaScript functionality
├── images/
│   └── logo_full.png  # Brand logo
└── README.md          # This file
```

## 🎨 Brand Colors

- **Orange**: #FFB347
- **Pink**: #E64A8C
- **Purple**: #8B4FD6
- **Blue**: #4FA3FF
- **Gradient**: Linear gradient using all four colors

## ✨ Features

- ✅ Fully responsive design (mobile, tablet, desktop)
- ✅ Modern gradient text and animations
- ✅ Smooth scrolling and transitions
- ✅ Mobile-friendly navigation menu
- ✅ Optimized performance (static HTML/CSS/JS)
- ✅ SEO-friendly structure
- ✅ Accessibility features

## 🚀 Deployment Options

### Option 1: Netlify (Recommended)

1. **Using Netlify Drop:**
   - Go to [app.netlify.com/drop](https://app.netlify.com/drop)
   - Drag and drop the `lms-landing` folder
   - Your site is live instantly!

2. **Using Netlify CLI:**
   ```bash
   npm install -g netlify-cli
   cd lms-landing
   netlify deploy --prod
   ```

3. **Custom Domain Setup:**
   - In Netlify dashboard, go to Domain Settings
   - Add your custom domain (e.g., `yourlms.com`)
   - Configure DNS records as instructed

### Option 2: Vercel

1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Deploy:**
   ```bash
   cd lms-landing
   vercel --prod
   ```

3. **Custom Domain:**
   - Add domain in Vercel dashboard
   - Update DNS records

### Option 3: GitHub Pages

1. **Create repository:**
   ```bash
   cd lms-landing
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/lms-landing.git
   git push -u origin main
   ```

2. **Enable GitHub Pages:**
   - Go to repository Settings
   - Navigate to Pages section
   - Select `main` branch as source
   - Save

3. **Custom Domain:**
   - Add `CNAME` file with your domain
   - Configure DNS:
     ```
     A Record: 185.199.108.153
     A Record: 185.199.109.153
     A Record: 185.199.110.153
     A Record: 185.199.111.153
     ```

### Option 4: Traditional Web Hosting (cPanel/FTP)

1. **Upload files via FTP:**
   - Connect to your hosting server
   - Upload all files to `public_html` or `www` directory
   - Maintain folder structure

2. **File Permissions:**
   - Set directories to 755
   - Set files to 644

## 🔗 Linking to Main App

The landing page links to your main application at:
- Login: `https://app.yourlms.com/login`
- Signup: `https://app.yourlms.com/signup`

**Before deploying**, update these links in all HTML files if your app URL is different:

1. **index.html** - Update all `href="https://app.yourlms.com/..."` links
2. **features.html** - Update navigation and CTA links
3. **pricing.html** - Update all signup and contact links

## 📝 Customization Guide

### Change Colors

Edit `css/style.css` and update CSS variables:
```css
:root {
    --color-orange: #FFB347;
    --color-pink: #E64A8C;
    --color-purple: #8B4FD6;
    --color-blue: #4FA3FF;
}
```

### Update Content

- **Homepage**: Edit `index.html`
- **Features**: Edit `features.html`
- **Pricing**: Edit `pricing.html`

### Change Logo

Replace `images/logo_full.png` with your logo (recommended size: 200x50px)

### Add Analytics

Add Google Analytics or other tracking code before `</head>` tag:
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

## 🔒 SSL/HTTPS

Most modern hosting platforms (Netlify, Vercel, GitHub Pages) provide free SSL certificates automatically.

For traditional hosting:
- Use Let's Encrypt (free)
- Enable HTTPS in cPanel
- Update app URLs to use `https://`

## 🌐 DNS Configuration

For custom domain (e.g., `yourlms.com`):

### Main Landing Page
```
Type: A Record
Host: @
Value: [Your hosting IP]
```

### App Subdomain
```
Type: CNAME
Host: app
Value: [Your app hosting domain]
```

Example final URLs:
- Landing: `https://yourlms.com`
- App: `https://app.yourlms.com`

## 📱 Testing

Test your landing page on:
- ✅ Desktop browsers (Chrome, Firefox, Safari, Edge)
- ✅ Mobile devices (iOS Safari, Android Chrome)
- ✅ Tablet devices
- ✅ Different screen sizes

Use Chrome DevTools to test responsiveness:
1. Open DevTools (F12)
2. Click device toggle (Ctrl+Shift+M)
3. Test various screen sizes

## ⚡ Performance Optimization

Current optimizations:
- Minified CSS (production-ready)
- Optimized images
- Lazy loading for images
- Smooth animations with CSS
- Minimal JavaScript footprint

Additional optimizations:
1. **Minify HTML**: Use [HTML Minifier](https://www.willpeavy.com/tools/minifier/)
2. **Compress Images**: Use [TinyPNG](https://tinypng.com/)
3. **Enable Caching**: Add `.htaccess` for Apache servers:
   ```apache
   <IfModule mod_expires.c>
     ExpiresActive On
     ExpiresByType image/png "access plus 1 year"
     ExpiresByType text/css "access plus 1 month"
     ExpiresByType text/javascript "access plus 1 month"
   </IfModule>
   ```

## 🐛 Troubleshooting

### Logo not showing
- Check file path: `images/logo_full.png`
- Verify file exists and is not corrupted
- Check file permissions (644)

### Mobile menu not working
- Ensure `js/main.js` is loaded
- Check browser console for JavaScript errors
- Verify `id="mobileMenuToggle"` exists in HTML

### Styling issues
- Clear browser cache (Ctrl+Shift+Delete)
- Verify `css/style.css` is linked correctly
- Check for CSS syntax errors

### Links not working
- Verify app URLs are correct
- Check for typos in href attributes
- Test in different browsers

## 📧 Support

For issues or questions:
- Check documentation in this README
- Review HTML/CSS comments
- Test in browser DevTools console

## 📄 License

This landing page is part of the LownDesk project.

---

**Version**: 1.0.0  
**Last Updated**: 2026  
**Built With**: HTML5, CSS3, Vanilla JavaScript
