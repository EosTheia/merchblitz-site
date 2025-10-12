# MerchBlitz Assets Directory

This directory contains all the creative assets for your MerchBlitz landing page.

## 📁 File Structure

```
/assets/
├── README.md (this file)
├── Sequential Carousel Assets/
│   ├── creative-tiktok-9x16.jpg
│   ├── creative-pdp-hero.jpg
│   ├── creative-ig-square.jpg
│   └── creative-email-1200x600.jpg
├── Library Hover Assets/
│   ├── poster-hero.jpg
│   ├── poster-ig.jpg
│   ├── poster-tiktok.jpg
│   ├── poster-badges.jpg
│   ├── poster-email.jpg
│   ├── hover-hero.mp4
│   ├── hover-ig.mp4
│   ├── hover-tiktok.mp4
│   ├── hover-badges.mp4
│   └── hover-email.mp4
├── Social Proof Avatars/
│   ├── avatar-1.jpg (customer 1)
│   ├── avatar-2.jpg (customer 2)
│   ├── avatar-3.jpg (customer 3)
│   └── ... (add more as needed)
└── Optional Video Assets/
    ├── creative-ugc-vertical.mp4
    └── creative-explainer.mp4
```

## 🎨 Sequential Carousel Assets

Replace the placeholder images in the main carousel with your actual creative examples:

### **Recommended Filenames & Dimensions:**
- `creative-tiktok-9x16.jpg` — **1080×1920** (TikTok/Reels format)
- `creative-pdp-hero.jpg` — **1920×800** or **1600×800** (Product page hero)
- `creative-ig-square.jpg` — **1080×1080** (Instagram square post)
- `creative-email-1200x600.jpg` — **1200×600** (Email header)

### **How to Update:**
1. Add your creative files to `/assets/` with the exact filenames above
2. Update the `items` array in `index.html` if you want to change keywords or captions:

```javascript
const items = [
  {
    keywords: ["TikTok", "9:16", "Black Friday", "Increase Engagement"],
    media: { type: "image", src: "/assets/creative-tiktok-9x16.jpg" },
    caption: "TikTok Promo — 1080×1920"
  },
  // ... other items
];
```

## 🎬 Adding Video Creatives (Optional)

To add video assets to the sequential carousel:

### **1. Add Video Element to HTML:**
In `index.html`, find the `.stageCreative` section and add:
```html
<figure class="stageCreative" id="stageCreative">
  <img id="stageImg" alt=""/>
  <video id="stageVid" muted playsinline loop style="display:none;"></video>
  <figcaption id="stageCaption"></figcaption>
</figure>
```

### **2. Uncomment Video Support in JavaScript:**
Find these commented lines in the `runLoop` function and uncomment:
```javascript
// Query the video element at the top:
// const vidEl = document.getElementById('stageVid');

// In the runLoop function:
// else if(item.media.type === 'video'){
//   imgEl.style.display='none';
//   vidEl.src = item.media.src; vidEl.style.display='block';
//   try{ await vidEl.play(); }catch(e){}
// }
```

### **3. Add Video Items:**
```javascript
{
  keywords: ["UGC", "Explainer", "Vertical"],
  media: { type: "video", src: "/assets/creative-ugc-vertical.mp4" },
  caption: "UGC Explainer — 1080×1920"
}
```

## 🖼️ Library Hover Assets

Replace the poster images and hover videos in the "Library" section:

### **Poster Images (Static):**
- `poster-hero.jpg` — Homepage hero example (800×450 recommended)
- `poster-ig.jpg` — Instagram example
- `poster-tiktok.jpg` — TikTok example  
- `poster-badges.jpg` — PDP badges example
- `poster-email.jpg` — Email header example

### **Hover Videos (Interactive):**
- `hover-hero.mp4` — Short demo of hero creation
- `hover-ig.mp4` — IG square creation demo
- `hover-tiktok.mp4` — TikTok creation demo
- `hover-badges.mp4` — Badge creation demo
- `hover-email.mp4` — Email header demo

**Keep hover videos SHORT (3-6 seconds) and small file size!**

## ⚡ Performance Guidelines

### **Images:**
- **Format**: JPEG (85% quality) or WebP
- **File Size**: Keep under 300-800 KB each
- **Optimization**: Use tools like TinyPNG or Squoosh

### **Videos:**
- **Format**: H.264 MP4 or WebM
- **File Size**: Keep under 3-6 MB each
- **Duration**: 3-6 seconds for hover videos
- **Settings**: 
  - Resolution: Match your target format (1080×1920, 1080×1080, etc.)
  - Frame Rate: 24-30 fps
  - Bitrate: ~1-2 Mbps for web

## 🔧 File Replacement Process

1. **Add your files** to the `/assets/` directory
2. **Use exact filenames** from the recommendations above, OR
3. **Update the paths** in `index.html` if using different names
4. **Test locally** by opening `index.html` in your browser
5. **Commit and push** to deploy:
   ```bash
   git add assets/
   git commit -m "Add brand creative assets"
   git push origin main
   ```

## 🎯 Brand Guidelines

When creating your assets:
- **Consistent branding** across all formats
- **High contrast** for readability
- **Clear call-to-actions** where appropriate
- **On-brand colors** matching your Shopify store
- **Professional quality** that represents your brand well

## 📝 Notes

- Current site uses placeholder images from Picsum and sample videos
- Replace placeholders gradually or all at once
- Keep backups of your original assets
- Test on mobile devices to ensure quality
- Monitor site performance after adding real assets

## 👤 Social Proof Avatar Management

### **Upload Process:**
1. **Prepare Images**: 
   - Size: 72×72px to 200×200px (will be cropped to circle)
   - Format: JPG or PNG
   - Quality: Professional headshots work best
   - Keep under 50KB each

2. **Naming Convention**:
   ```
   avatar-1.jpg  → First testimonial (Lina Martinez)
   avatar-2.jpg  → Second testimonial (Tom Chen) 
   avatar-3.jpg  → Third testimonial (Maya Singh)
   ```

3. **Update HTML**: Find the testimonial section and replace:
   ```html
   <!-- Change this: -->
   <div class="quote-avatar">LM</div>
   
   <!-- To this: -->
   <div class="quote-avatar">
     <img src="/assets/avatars/avatar-1.jpg" alt="Lina Martinez">
   </div>
   ```

### **Custom Testimonials**:
To add your own testimonials, edit the HTML in the `.marquee` section:

```html
<div class="quote">
  <div class="quote-text">Your customer's testimonial text here...</div>
  <div class="quote-author">
    <div class="quote-avatar">
      <img src="/assets/avatars/avatar-your-name.jpg" alt="Customer Name">
    </div>
    <div class="quote-details">
      <div class="quote-name">Customer Full Name</div>
      <div class="quote-company">Their Company Name</div>
    </div>
  </div>
</div>
```

## 🎨 Sequential Carousel Management

### **Complete Asset Replacement Process:**

1. **Create Your Assets** (in design tools like Figma/Canva):
   - TikTok: 1080×1920 (9:16 ratio)
   - PDP Hero: 1920×800 or 1600×800 (2.4:1 ratio)
   - Instagram: 1080×1080 (1:1 ratio)  
   - Email: 1200×600 (2:1 ratio)

2. **Upload to `/assets/`** with exact names:
   ```
   creative-tiktok-9x16.jpg
   creative-pdp-hero.jpg
   creative-ig-square.jpg
   creative-email-1200x600.jpg
   ```

3. **Update the items array** in `index.html` (around line 265):
   ```javascript
   const items = [
     {
       keywords: ["Your", "Custom", "Keywords", "Here"],
       media: { type: "image", src: "/assets/creative-tiktok-9x16.jpg" },
       caption: "Your Custom Caption"
     },
     // ... repeat for other items
   ];
   ```

4. **Customize Keywords & Captions**: 
   - `keywords`: 4 words that describe the creative
   - `caption`: Brief description of the asset format

### **Testing Your Assets:**
1. Upload files to `/assets/`
2. Open your site locally or on GitHub Pages
3. Check browser developer tools for any 404 errors
4. Verify images load smoothly in the carousel

---

**Need help?** The current `index.html` file has all the integration points marked with comments for easy updating.