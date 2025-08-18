# Deployment Guide for Ignatius Gallery Website

## Current Setup
Your website now has:
- **Main Portfolio** (`index.html`) - Showcases Gasson Hall photogrammetry vs NeRF work
- **St. Ignatius Page** (`st-ignatius.html`) - Overview of your splat rendering work
- **3D Viewer** (`viewer.html`) - Full-screen interactive Ignatius viewer
- **Unified Navigation** - Easy switching between all sections

## Deploying to Vercel

### 1. Push to GitHub
```bash
git add .
git commit -m "Merge portfolio with 3D viewer"
git push origin main
```

### 2. Deploy on Vercel
- Connect your GitHub repo to Vercel
- Vercel will automatically detect it's a static site
- Build command: (none needed)
- Output directory: `/` (root)
- Deploy!

## Integrating Cloudflare Bucket Assets

### Current Asset Setup
Your `vercel.json` is already configured to proxy assets from:
```
https://pub-152c6406dde64b469258f1ce7228b176.r2.dev/
```

### To Use Your Cloudflare Bucket Instead:

1. **Update `vercel.json`** - Replace the R2 URL with your Cloudflare bucket:
```json
{
  "rewrites": [
    { "source": "/", "destination": "/index.html" },
    {
      "source": "/assets/(.*)",
      "destination": "https://your-cloudflare-bucket.com/$1"
    }
  ]
}
```

2. **High-Quality Asset Integration**:
   - Upload your high-res assets to Cloudflare
   - Reference them in your HTML like: `/assets/your-asset.jpg`
   - Vercel will proxy them through your bucket

### Example Asset Usage:
```html
<!-- In your portfolio pages -->
<img src="/assets/high-res-gasson.jpg" alt="Gasson Hall High Resolution">

<!-- In your 3D viewer -->
<script>
  // Your .ksplat files can be hosted on Cloudflare
  const sceneConfig = {
    photorealistic: [{
      'path': '/assets/caudell_photorealistic_ignatius.ksplat',
      'splatAlphaRemovalThreshold': 5
    }]
  };
</script>
```

## File Structure After Merge
```
/
├── index.html              # Main portfolio (Gasson Hall)
├── st-ignatius.html        # St. Ignatius overview
├── viewer.html             # Full-screen 3D viewer
├── style.css               # Shared styling
├── vercel.json             # Vercel configuration
├── assets/                 # Local assets
│   ├── CSI_logo.png
│   ├── *.ksplat files
│   └── lib/ (Three.js, Gaussian Splats)
└── Cloudflare Bucket       # High-quality assets
    ├── high-res-images/
    ├── videos/
    └── 3d-models/
```

## Benefits of This Setup

1. **Professional Portfolio** - Showcases your work professionally
2. **Interactive 3D Experience** - Full-screen viewer for immersive experience
3. **High-Quality Assets** - Cloudflare bucket for fast, high-res content
4. **Unified Navigation** - Seamless experience between sections
5. **Vercel Hosting** - Fast, reliable deployment with CDN

## Next Steps

1. **Deploy to Vercel** - Get your site live
2. **Upload High-Quality Assets** - Move large files to Cloudflare
3. **Update Asset References** - Point to your Cloudflare bucket
4. **Test Everything** - Ensure navigation and viewer work smoothly

Your Ignatius viewer is seriously impressive - being able to switch between photorealistic and watercolor styles in real-time is next-level stuff! 🎨✨
