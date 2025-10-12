# MerchBlitz Assets Directory

This directory contains all the visual and media assets for the MerchBlitz website.

## Required Files:

### Video Assets
- `hero-loop.mp4` - Hero section background video (16:9 aspect ratio, ~8-12MB, no audio, muted + playsinline for mobile autoplay)
- `hero-loop.webm` - Optional WebM version for better browser support

### Open Graph & Social Media Images
- `og-1200x630.png` - Facebook/LinkedIn Open Graph image (1200×630px)
- `og-1200x628.png` - Twitter/X large card image (1200×628px, ~1.91:1 ratio)

### Icons & Favicons
- `favicon.ico` - Multi-size ICO file for browsers
- `apple-touch-icon.png` - Apple touch icon (180×180px)
- `android-chrome-192x192.png` - Android chrome icon (192×192px)
- `android-chrome-512x512.png` - Android chrome icon (512×512px)

## Asset Guidelines:

### Hero Video
- Format: MP4 (primary), WebM (optional)
- Aspect Ratio: 16:9
- Duration: 5-15 seconds (looping)
- Size: Keep under 12MB for performance
- Audio: None (muted autoplay)
- Content: Should show "pain → fix" montage demonstrating the problem MerchBlitz solves

### Social Images
- Start with 1024×1024 master design
- Crop/resize to required dimensions
- Include MerchBlitz branding and value proposition
- Use brand colors: Ink #0B1020, Bolt Blue #2563EB, Lightning Yellow #F5B600

### Icons
- Start with 1024×1024 PNG master
- Should feature "MB" monogram with lightning-bolt motif
- Downscale to required sizes
- Maintain clarity at small sizes

## How to Add Assets:

1. Create your master assets (video, social images, icons)
2. Process them to the required specifications above
3. Replace this README with the actual asset files
4. Update any placeholder references in the HTML files

## Testing Social Sharing:

After adding og-1200x630.png and og-1200x628.png:
1. Test Facebook sharing: https://developers.facebook.com/tools/debug/
2. Test Twitter cards: https://cards-dev.twitter.com/validator
3. Ensure images aren't cropped badly in previews