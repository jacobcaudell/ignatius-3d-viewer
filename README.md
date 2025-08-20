# Caudell Spatial Intelligence - 3D Visualization Portfolio

A showcase of advanced 3D reconstruction and visualization technologies, featuring architectural heritage projects and interactive 3D experiences.

## Projects

### Gasson Hall: Two Approaches to 3D Reconstruction
A comparison of classical photogrammetry (Metashape) and NeRF training (Nerfstudio) workflows using drone imagery from Boston College's Gasson Hall (1913). Demonstrates the range of possibilities in architectural visualization from structural accuracy to view-dependent lighting and novel viewpoint synthesis.

### St. Ignatius: Interactive 3D Gaussian Splatting
Real-time 3D visualization using Gaussian Splatting technology to explore Pablo Eduardo's 2005 sculpture. Features dual artistic styles (photorealistic and watercolor) with interactive camera controls for immersive exploration.

### Pondside Green: Terrain Modeling & Analysis
Large-scale terrain modeling project demonstrating precision environmental analysis. Combines systematic drone capture with decision-grade ground control to deliver high-fidelity terrain models for golf course redesign and construction planning. Features optimized MP4 video format for universal browser compatibility.

## Technology Stack

- **Drone Capture**: DJI Matrice 4 Enterprise
- **Photogrammetry**: Metashape Pro with local processing
- **Neural Rendering**: Nerfstudio with NeRF technology
- **Real-time Rendering**: Gaussian Splatting for interactive 3D
- **Web Technologies**: Three.js, modern ES6 modules
- **Deployment**: Vercel with Cloudflare R2 asset hosting

## Project Structure

```
caudell_spatial_intelligence_vercel_site/
├── index.html              # Home page with service overview
├── services.html           # Professional services overview with proof stripe
├── about.html              # Company and founder information
├── contact.html            # Contact form and information
├── terrain-modeling.html   # Pondside Green terrain analysis project
├── gasson-hall.html        # Gasson Hall project page
├── st-ignatius.html        # St. Ignatius project page with embedded viewer
├── viewer.html             # Full-screen 3D viewer with navigation
├── viewer-embedded.html    # Embedded 3D viewer for iframe integration
├── style.css               # Shared styling and responsive design
├── vercel.json             # Vercel deployment configuration
├── README.md               # This documentation

└── assets/
    ├── CSI_logo.png        # Company logo
    ├── founder_hero_shot.png   # Founder portrait
    ├── occ_18_green_heat_map.png      # Terrain altitude heatmap
    ├── occ_18_green_tight_flythrough.mov   # Terrain flythrough video
    └── lib/                 # Three.js and Gaussian Splats libraries
        ├── three.module.js
        └── gaussian-splats-3d.module.js
```

## Features

### Services Overview
- **Terrain & Environmental Models**: High-fidelity ground models with slope, contour, and flow analysis
- **3D Reality Capture**: Drone-based site capture with professional workflows
- **Interactive 3D Experiences**: Immersive browser-based models for intuitive reviews

### Gasson Hall Project
- **Classical Photogrammetry**: High-fidelity mesh reconstruction with UV-mapped textures
- **NeRF Training**: Neural radiance field representation for view-dependent lighting and novel viewpoints
- **Professional Output**: Cinematic flythroughs with post-processing
- **Local Processing**: High-performance local processing with Metashape Pro

### St. Ignatius Project
- **Real-time Rendering**: Interactive 3D visualization with Gaussian Splatting
- **Dual Artistic Styles**: Switch between photorealistic and watercolor interpretations
- **Intuitive Controls**: Mouse orbit, right-click pan, scroll zoom
- **Embedded Integration**: Seamless iframe integration for portfolio pages
- **Error Handling**: Automatic fallback to Blurry link for compatibility issues
- **Cross-platform Support**: Robust detection and graceful degradation

### Terrain Modeling
- **Large-scale Coverage**: 200+ acres of terrain modeling
- **Quality Control**: Professional workflows with ground control validation
- **Decision-grade Outputs**: Ready for design and construction planning
- **Fast Turnaround**: On-site processing delivered within 24 hours

## Website Structure

The website presents a cohesive narrative from service overview to interactive experience:

1. **Home Page** (`index.html`): Service overview with case study links
2. **Services Page** (`services.html`): Professional services with proof stripe and service cards
3. **Portfolio Pages**: Individual project showcases with case study CTAs
4. **Interactive Experience** (`st-ignatius.html`): Embedded 3D viewer demonstrating real-time capabilities
5. **Full-screen Viewer** (`viewer.html`): Immersive experience with navigation back to portfolio
6. **Unified Navigation**: Seamless movement between all sections

## Deployment

### Vercel Deployment
1. Connect your GitHub repository to Vercel
2. Vercel automatically detects static site (no build command needed)
3. Assets are proxied through Cloudflare R2 for high-quality content delivery
4. Custom headers ensure proper CORS and caching

### Local Development
```bash
# Python
python3 -m http.server 8000

# Node.js
npx serve .

# PHP
php -S localhost:8000
```

## Technical Details

### 3D Reconstruction Pipeline
1. **Drone Capture**: High-resolution imagery with precise positioning
2. **Image Processing**: Local high-performance processing for computational efficiency
3. **Workflow Integration**: Seamless data transfer between Metashape Pro and Nerfstudio
4. **Output Generation**: Professional-grade visualizations and interactive experiences

### Error Handling & Compatibility
1. **Automatic Detection**: Timeout and content validation for 3D viewer failures
2. **Graceful Fallbacks**: Seamless transition to alternative viewing options
3. **User Guidance**: Technical explanations and actionable recommendations
4. **Cross-platform Support**: Robust handling of WebGL and graphics limitations

### Gaussian Splatting Implementation
- **Real-time Performance**: Optimized for smooth 60fps rendering
- **Scene Management**: Dynamic loading and switching between artistic styles
- **Camera Controls**: Intuitive navigation with orbit, pan, and zoom
- **Responsive Design**: Optimized for all device sizes

## Asset Management

- **Local Assets**: CSS, HTML, JavaScript libraries
- **Cloud Assets**: High-resolution videos and 3D models via Cloudflare R2
- **Video Optimization**: MP4 conversion for web compatibility (77% size reduction)
- **Optimization**: Efficient loading with proper caching headers
- **Quality**: Professional-grade content delivery
- **Format Support**: Web-standard formats for universal compatibility

## Browser Compatibility

- **Modern Browsers**: Chrome, Firefox, Safari, Edge (latest versions)
- **WebGL Support**: Required for 3D rendering
- **ES6 Modules**: Modern JavaScript for optimal performance
- **Responsive Design**: Mobile and desktop optimized
- **Video Compatibility**: MP4 format for universal browser support
- **Graceful Degradation**: Automatic fallbacks for unsupported features

## License

© 2025 Caudell Spatial Intelligence

---

*This portfolio demonstrates the intersection of architectural heritage preservation, cutting-edge 3D technology, and artistic interpretation through innovative visualization techniques.*
