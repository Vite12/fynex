# Fynex Discord Bot Website

A modern, responsive website for the Fynex Discord bot featuring chat rewards, giveaways, and community engagement tools.

## 🚀 Deploy to Netlify

This website is fully configured for Netlify deployment.

### Quick Deploy
1. **Fork or download** this repository
2. **Connect to Netlify:**
   - Go to [netlify.com](https://netlify.com) and sign up (free)
   - Click "New site from Git" 
   - Connect your GitHub repository
3. **Configure build settings:**
   - Build command: `npm run build`
   - Publish directory: `dist/public`
   - Base directory: `.` (root)
4. **Deploy!** Netlify will automatically build and host your site

### Manual Deploy
1. Run `npm run build` to build the static files
2. Upload the `dist/public` folder contents to Netlify via drag & drop

## 📁 Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/         # Website pages (home, privacy, terms)
│   │   └── assets/        # Images and static files
│   └── index.html         # HTML template with SEO meta tags
├── netlify.toml           # Netlify configuration
└── dist/public/           # Built static files (generated)
```

## ✨ Features

- **Modern Design** - Red theme with smooth animations
- **Responsive** - Works on all devices
- **SEO Optimized** - Proper meta tags for search engines
- **Fast Loading** - Optimized assets and caching headers
- **React SPA** - Single page application with client-side routing
- **Pages:**
  - Homepage with bot features
  - Privacy Policy
  - Terms of Service

## 🛠️ Development

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 🌐 Live Website

Once deployed to Netlify, your website will be available at:
`https://your-site-name.netlify.app`

You can also add a custom domain in the Netlify dashboard.

## 📝 Customization

To customize for your Discord bot:

1. **Update Discord URLs** in these files:
   - `client/src/components/hero-section.tsx`
   - `client/src/components/header.tsx` 
   - `client/src/components/cta-section.tsx`
   - `client/src/components/footer.tsx`

2. **Replace placeholder URLs:**
   - `YOUR_BOT_ID` - Your Discord bot's client ID
   - `YOUR_PERMISSIONS` - Required bot permissions
   - `YOUR_SUPPORT_SERVER` - Your Discord support server invite

3. **Update meta tags** in `client/index.html`:
   - Website URL
   - Bot description
   - Social media image

## 📊 Performance

- **Build size:** ~285 KB JavaScript + 66 KB CSS (gzipped: ~90 KB + 11 KB)
- **Images:** Optimized WebP and PNG formats
- **Caching:** Long-term caching for static assets
- **CDN:** Global distribution via Netlify

---

Built with React, TypeScript, Tailwind CSS, and ❤️