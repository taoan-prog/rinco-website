# Rinco International - Sustainable Bags Website

Professional company website for Rinco International Co., Ltd., featuring sustainable bag products made from RPET and other eco-friendly materials.

## 🎯 Features

- **Fully responsive** - Optimized for all devices
- **Modern design** - Clean, corporate aesthetic
- **SEO optimized** - Semantic HTML, meta tags, structured content
- **Fast loading** - Pure HTML/CSS/JS, no external dependencies
- **Interactive** - Smooth scrolling, mobile menu, scroll animations, form validation
- **Accessible** - ARIA labels, keyboard navigation, semantic markup

## 📁 Project Structure

```
cloudflare-site/
├── index.html      Main company website
├── style.css       Responsive styles & animations
├── script.js       Interactive features
├── _redirects      URL redirect rules (optional)
├── _headers        Security headers (optional)
└── README.md       This documentation
```

## 🚀 Deploy to Cloudflare Pages (3 Steps)

### Step 1: Push to Git
```bash
cd ~/.openclaw/workspace/telegram3/cloudflare-site

# Initialize repository
git init
git add .
git commit -m "Initial commit - Rinco International sustainable bags website"

# Create repository on GitHub/GitLab/Bitbucket
# Then push:
git remote add origin https://github.com/yourusername/rinco-site.git
git branch -M main
git push -u origin main
```

### Step 2: Connect Cloudflare Pages
1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com) → **Pages**
2. Click **Create a project**
3. Connect your Git provider and select the repository
4. Configure build settings:
   - **Production branch**: `main`
   - **Build command**: *(leave empty)*
   - **Build output directory**: `/`
5. Click **Save and Deploy**

### Step 3: Get Your URL
After ~2 minutes, your site will be live at:
```
https://rinco-site.pages.dev
```

## 📋 Content Overview

### Website Sections

1. **Hero** - Brand tagline "Designed for beauty, Crafted with care" + client logos
2. **About** - Company intro, stats, Shenzhen HQ + Anhui factory contact cards
3. **Why RPET?** - 4 sustainability benefits with icons
4. **Materials** - All RPET variants + codes (9 types), plus Recycled Cotton, Paper Straw (FSC), Heat Resistant
5. **Products** - 6 product categories with material codes
6. **Certifications** - ISO 9001, ISO 14001, SEDEX, Ecovadis, GRS + third-party auditors
7. **Clients** - L'Oréal, LVMH, Estée Lauder, Avon, Walmart
8. **CTA** - Partner invitation
9. **Contact** - Inquiry form + full contact info
10. **Footer** - Navigation + brand + eco badge

### Material Codes Included

All product codes from the PDF catalog are listed:

| Material | Codes |
|----------|-------|
| RPET Canvas | #44776R1, #35802R9, #47502 |
| RPET Sherpa | #22065, #51048R13A |
| RPET Oxford | #45537R6 |
| RPET Satin | #47992A |
| RPET Velvet | #44680R1B |
| RPET Corduroy | #48656 |
| RPET Terry | #48632B, #48406M, #49779, #49778A, #46182 |
| RPET Mesh | #24171, #23047 |
| RPET Neoprene | #23157 |
| Recycled Cotton | #23165, #46837A, #46593, #45743R3A, #45479R1 |
| Paper Straw (FSC) | #46875, #53908C, #47604B, #46679R1B, #46876A |
| Heat Resistant | #46062R4A, #56041, #44006R2A, #44027R2A |
| Other Products | Multiple showcase codes (see Products section) |

## 🎨 Customization

### Update Contact Info
Edit `index.html` and modify:
- Shenzhen HQ address
- Email: `judy@travelmate21.com` (already set)
- Website: `www.rinco-intl.com` (already linked)
- Factory address (already included)

### Change Colors
Edit CSS variables in `style.css` `:root` section:
```css
--primary: #1a5f4a;      /* Main green */
--secondary: #c0845c;    /* Accent orange */
--accent: #e9c46a;       /* Highlight yellow */
```

### Add Real Product Images
Currently uses icon-based product placeholders. Replace with actual product photos:
- Update `.product-image` backgrounds or add `<img>` tags
- Recommended: 600×600px JPG/WebP images
- Host images locally or use Cloudflare Images/CDN

### Form Backend Integration
Current form shows demo success message. To receive real inquiries:

**Option 1: Web3Forms (Free 2500/month)**
```javascript
// In script.js form submit handler:
const response = await fetch('https://api.web3forms.com/submit', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
        access_key: 'YOUR_ACCESS_KEY',
        ...data
    })
});
```

**Option 2: EmailJS (Free 200/month)**
```javascript
await EmailJS.send({
    service_id: 'YOUR_SERVICE',
    template_id: 'YOUR_TEMPLATE',
    user_id: 'YOUR_USER',
    template_params: data
});
```

**Option 3: Cloudflare Workers + D1**
- Create a Worker that writes to D1 database
- Free tier: 100,000 requests/day

## 📱 Mobile Responsive

- ✅ Desktop (1200px+): Full layout
- ✅ Tablet (768-1024px): Adjusted grid
- ✅ Mobile (<768px): Hamburger menu, stacked layout
- ✅ Small mobile (<480px): Optimized spacing

## 🔧 Local Development

```bash
# Using Python
cd ~/.openclaw/workspace/telegram3/cloudflare-site
python3 -m http.server 8000
# Visit http://localhost:8000

# Using Node.js
npx http-server . -p 8000
```

## 📊 SEO & Performance

- ✅ Zero external CSS/JS dependencies
- ✅ Google Fonts preconnect for fast loading
- ✅ Semantic HTML5 structure
- ✅ Meta description + viewport
- ✅ Open Graph tags ready to add
- ✅ Image alt text for accessibility
- ✅ Lazy loading ready (IntersectionObserver)

## 📝 Notes

- All material codes from PDF catalog are included
- Client logos are text-based (L'Oréal, LVMH, etc.)
- Contact form currently in demo mode
- Replace placeholder content with real data as needed
- Add Google Analytics tracking if desired

## 🌱 Deploy Status

- **Status**: Ready ✅
- **Build time**: ~30 seconds
- **Total size**: ~55KB (HTML+CSS+JS)
- **Compatibility**: All modern browsers (Chrome, Firefox, Safari, Edge)

---

**Website built for Rinco International Co., Ltd.**
**Sustainable bags - Designed for beauty, crafted with care**
