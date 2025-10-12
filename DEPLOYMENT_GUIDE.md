# MerchBlitz Website - Deployment & Testing Guide

## ✅ Completed Implementation

### 🏗️ Structure Complete
- ✅ All required HTML pages created and properly structured
- ✅ `/assets/` directory created with documentation
- ✅ Footer navigation links to all pages
- ✅ Custom 404.html for GitHub Pages

### 🔧 Technical Features Implemented
- ✅ Google Analytics with Consent Mode (default denied)
- ✅ Cookie consent banner (vanilla-cookieconsent)
- ✅ Email signup form (Google Forms integration)
- ✅ Countdown timer to BFCM deadline (2025-11-30T23:59:59+03:00)
- ✅ Responsive dark theme design
- ✅ WCAG 2.2 AA accessibility considerations

### 📱 Social Media & SEO
- ✅ Open Graph tags with proper dimensions (1200×630)
- ✅ Twitter Card meta tags (1200×628)
- ✅ Structured sitemap.xml
- ✅ robots.txt with sitemap reference
- ✅ Proper favicon structure

## 🎯 Next Steps - What You Need To Do

### 1. Create Visual Assets
You need to create these files in the `/assets/` folder:

#### Required Video:
- `hero-loop.mp4` - Hero background video (16:9, ~8-12MB, no audio)
- `hero-loop.webm` - Optional WebM version for better browser support

#### Required Images:
- `og-1200x630.png` - Facebook/LinkedIn Open Graph image
- `og-1200x628.png` - Twitter/X card image
- `favicon.ico` - Multi-size favicon
- `apple-touch-icon.png` - Apple touch icon (180×180px)
- `android-chrome-192x192.png` - Android icon (192×192px)
- `android-chrome-512x512.png` - Android icon (512×512px)

📋 **Detailed specifications are in `/assets/README.md`**

### 2. Deploy to GitHub Pages
```bash
# In your repository root:
git add .
git commit -m "Complete MerchBlitz website implementation"
git push origin main
```

#### GitHub Pages Setup:
1. Go to your repo Settings > Pages
2. Source: Deploy from branch `main` / root
3. Custom domain: `merchblitz.com` (already configured in CNAME)
4. Ensure DNS points to GitHub Pages

### 3. Test Everything

#### 🧪 Functional Testing
- [ ] Visit `https://merchblitz.com` (or your GitHub Pages URL)
- [ ] Test email signup form submission
- [ ] Verify countdown timer is running
- [ ] Check all footer links work
- [ ] Test 404 page by visiting non-existent URL
- [ ] Verify cookie consent banner appears and functions

#### 📊 Analytics Testing
1. **Open GA4 Real-time reports**
2. **Visit your site** - Should see NO activity (consent denied)
3. **Accept cookies** - Should see activity appear
4. **Check Consent Debug view** in GA4 for proper consent signals

#### 🔍 Social Media Testing
1. **Facebook Sharing Debugger**: https://developers.facebook.com/tools/debug/
   - Enter your URLs
   - Verify og-1200x630.png displays correctly
2. **Twitter Card Validator**: https://cards-dev.twitter.com/validator
   - Verify og-1200x628.png displays correctly

#### 📱 Mobile Testing
- [ ] Test on iOS Safari, Android Chrome
- [ ] Verify video autoplays (muted)
- [ ] Check responsive layout
- [ ] Test form submission on mobile

### 4. SEO Setup

#### Submit Sitemap:
1. **Google Search Console**: https://search.google.com/search-console
2. Add property for `merchblitz.com`
3. Submit sitemap: `https://merchblitz.com/sitemap.xml`

#### Monitor Indexing:
- Check which pages get indexed
- Monitor for any crawling errors
- Verify proper Open Graph previews

## 🐛 Troubleshooting

### Cookie Consent Not Working?
- Check browser console for JavaScript errors
- Verify CDN links are loading properly
- Test in incognito mode

### Analytics Not Tracking?
- Confirm GA4 property ID: `G-DP347K6GVM`
- Check consent was granted
- Use GA4 DebugView for real-time troubleshooting

### Video Not Autoplaying?
- Ensure video file is under 12MB
- Check `muted`, `playsinline`, `autoplay` attributes
- Test on different devices/browsers

### Social Sharing Issues?
- Verify image files exist and are accessible
- Check image dimensions match specifications
- Use debugging tools to clear cache

## 📈 Performance Checklist
- [ ] Video file size optimized (< 12MB)
- [ ] Images compressed appropriately
- [ ] CSS/JS minified for production
- [ ] Test loading speed across devices

## 🔒 Legal Compliance
- [ ] Privacy policy reviewed and accurate
- [ ] Cookie policy reflects actual usage
- [ ] CCPA compliance page functional
- [ ] Terms of service completed (currently placeholder)

## 🎊 You're Ready to Launch!

Once you've completed the steps above, your MerchBlitz website will be fully functional and compliant with modern web standards. The site is built for high conversion with proper analytics tracking and legal compliance.

Remember to regularly test the email signup flow and monitor your GA4 analytics to optimize for better performance!