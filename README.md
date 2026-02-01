# Pantra Marketing Site

The official marketing and policy website for Pantra, a consumer app that prevents food waste by scanning grocery receipts and tracking pantry inventory.

## 🍃 About Pantra

Pantra is a U.S.-based startup with a mission: **Keep food fresh, cut waste, save money.** We help households reduce food waste through:

- **Receipt OCR scanning** - Automatically extract items from grocery receipts
- **Expiration tracking** - Never let food spoil again
- **Household sharing** - Keep everyone in sync
- **Personalized reminders** - Smart notifications tailored to your habits
- **AI pantry suggestions** - Meal ideas based on what you have

**What we're NOT:** Pantra is not a delivery service, meal kit provider, recipe blog, or in-person pickup service.

## 📁 Site Structure

- `index.html` - Main landing page with hero, features (3-column grid), testimonials, and CTAs
- `privacy.html` - Privacy policy detailing how we handle receipt images, account info, and notifications
- `terms.html` - Terms of service covering user obligations, acceptable use, and liability
- `styles.css` - Warm, sustainable design with sage green and soft cream palette
- `.well-known/apple-developer-domain-association.txt` - Apple domain verification placeholder

## 🎨 Design Features

- **Warm Color Palette:** Sage green (#7c9473) and soft cream (#f5f1e8)
- **Google Fonts:** Manrope (headings) + Work Sans (body text)
- **Mobile-First:** Responsive breakpoints at 768px and 480px
- **Sustainable Aesthetic:** Reflects our environmental mission
- **Zero External Dependencies** (except Google Fonts)

## 🚀 Deploying to GitHub Pages

### Quick Setup

1. Go to your repository **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Choose your branch (e.g., `main`) and select the root folder `/`
4. Click **Save**

Your site will be live at: `https://[username].github.io/Pantra-site/`

### Custom Domain (Optional)

1. In GitHub Pages settings, enter your custom domain
2. Add a `CNAME` file to the repository root with your domain
3. Configure DNS at your provider:
   - **A records** (for apex domain like `pantra.com`):
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - **CNAME record** (for `www.pantra.com`): Point to `[username].github.io`

## 🛠️ Local Development

```bash
# Clone the repository
git clone https://github.com/[username]/Pantra-site.git
cd Pantra-site

# Start a local server
python3 -m http.server 8000
# OR
npx http-server

# Visit in browser
open http://localhost:8000
```

## 📝 Updating Content

### Landing Page
- **Hero headline:** Edit `<h1>` in the `.hero` section
- **Features:** Modify feature cards in `#features` and `.features-alt` sections
- **Testimonials:** Update quotes in the `.testimonials` section
- **CTAs:** Change button text/links in `.cta-buttons`

### Privacy Policy
Customize sections related to:
- Receipt image handling
- Account data collection
- Notification preferences
- Data sharing policies

### Terms of Service
Update sections for:
- User obligations
- Acceptable use
- Service scope (what Pantra is/isn't)
- Liability limitations

### Styling
Edit CSS custom properties in `styles.css`:
```css
:root {
  --sage-green: #7c9473;
  --cream: #f5f1e8;
  /* ... */
}
```

### Apple Domain Verification
Replace the TODO content in `.well-known/apple-developer-domain-association.txt` with your actual Apple Developer Domain Association file.

## ✅ Pre-Deployment Checklist

- [ ] Replace Apple domain association TODO with actual content
- [ ] Test all internal links
- [ ] Verify mobile responsiveness
- [ ] Check color contrast for accessibility
- [ ] Update contact email addresses if needed
- [ ] Test on multiple browsers

## 📄 License

All rights reserved © 2026 Pantra
