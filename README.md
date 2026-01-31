# Pantra Marketing Site

The official marketing and policy website for the Pantra app.

## 📁 Site Structure

- `index.html` - Main landing page with hero section, features, and CTAs
- `privacy.html` - Privacy policy page
- `terms.html` - Terms of service page
- `styles.css` - Shared stylesheet with mobile-friendly, modern typography
- `.well-known/apple-developer-domain-association.txt` - Apple domain association file

## 🚀 Deploying to GitHub Pages

### Quick Setup (Recommended)

1. Go to your repository settings on GitHub
2. Navigate to **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch**
4. Choose the `main` branch (or your default branch)
5. Select the root folder `/` as the source
6. Click **Save**

Your site will be published at: `https://[username].github.io/Pantra-site/`

### Custom Domain (Optional)

If you want to use a custom domain:

1. In the GitHub Pages settings, enter your custom domain (e.g., `pantra.com`)
2. Add a `CNAME` file to the repository root containing your domain name
3. Configure your DNS provider:
   - For apex domain (pantra.com): Add A records pointing to GitHub's IP addresses
   - For subdomain (www.pantra.com): Add a CNAME record pointing to `[username].github.io`

GitHub's IP addresses for A records:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

### Verification

After deployment:
- Visit your GitHub Pages URL
- Verify all pages load correctly (index, privacy, terms)
- Test on mobile devices to confirm responsive design
- Check that all internal links work

## 🛠️ Local Development

To preview the site locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/[username]/Pantra-site.git
   cd Pantra-site
   ```

2. Open `index.html` in your browser, or use a local server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   ```

3. Visit `http://localhost:8000` in your browser

## 📝 Updating Content

- **Hero section**: Edit the `<section class="hero">` in `index.html`
- **Features**: Modify the feature cards in the `<section id="features">` 
- **Privacy Policy**: Update sections in `privacy.html`
- **Terms of Service**: Update sections in `terms.html`
- **Styling**: Customize colors and spacing in `styles.css` (see CSS variables at the top)
- **Apple Domain Association**: Replace the TODO text in `.well-known/apple-developer-domain-association.txt` with your actual Apple Developer content

## 🎨 Design Features

- **Mobile-first responsive design** - Works great on all devices
- **Modern typography** - Clean, readable system fonts
- **Accessible color contrast** - WCAG compliant colors
- **Fast loading** - No external dependencies, pure HTML/CSS
- **SEO-friendly** - Proper meta tags and semantic HTML

## 📄 License

All rights reserved © 2026 Pantra
