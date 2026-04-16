# Personal Website

A clean, Pythonic personal website built with MkDocs and Material Design theme. Features a professional portfolio showcasing work, projects, and blog content.

## 📁 Project Structure

```
.
├── docs/                           # Main documentation source
│   ├── index.md                   # Home page (About Me)
│   ├── work.md                    # Work experience page
│   ├── project.md                 # Projects portfolio index
│   ├── contact.md                 # Contact information
│   ├── images/                    # All images, photos, logos
│   │   ├── profile-placeholder.svg # Profile photo placeholder
│   │   ├── yo2.png               # Logo (to be added)
│   │   └── logo_fam.png          # Favicon (to be added)
│   ├── css/                       # Custom stylesheets
│   │   └── custom.css            # Custom styling and components
│   ├── blog/                      # Blog content
│   │   ├── index.md              # Blog main page
│   │   ├── 2026-01-15-production-ml.md      # Sample post
│   │   ├── 2026-01-10-data-pipeline.md      # Sample post
│   │   ├── 2026-01-05-scalable-analytics.md # Sample post
│   │   ├── categories/           # Blog categories
│   │   │   ├── ai-ml.md
│   │   │   ├── data-engineering.md
│   │   │   ├── product-strategy.md
│   │   │   └── technical.md
│   │   ├── tags/                 # Blog tag index
│   │   │   └── index.md
│   │   └── archive/              # Blog archive by year
│   │       ├── index.md
│   │       └── 2026.md
│   └── projects/                 # Detailed project pages
│       ├── criclytics.md
│       ├── data-pipeline.md
│       └── ai-product.md
├── overrides/                     # MkDocs theme customization
│   └── main.html                 # Custom sidebar with profile section
├── mkdocs.yml                     # MkDocs configuration
└── README.md                      # This file
```

## 🎨 Key Features

### 1. **Left Pane Profile Section**
- Profile photo placeholder (120x120px circular)
- Quick bio/title section
- Recent posts quick links
- Contact information
- Integrated with MkDocs Material theme sidebar

### 2. **Sticky Top Navigation**
- Mirrors the left sidebar structure
- Features emoji icons for visual appeal
- Automatically generated from nav configuration
- Responsive design for mobile/tablet

### 3. **Organized Content**
- **Work**: Professional experience page
- **Projects**: Portfolio with 3 detailed example projects
- **Blog**: Full blog system with:
  - Multiple posts (date-based naming)
  - Category organization
  - Tag system
  - Archive by year
- **Contact**: Contact information and links

### 4. **Professional Styling**
- Responsive design (desktop, tablet, mobile)
- Dark mode support
- Hover effects and animations
- Project cards with interactive features
- Optimized typography and spacing

## 🚀 How to Use

### Setup
```bash
# Install MkDocs and Material theme
pip install mkdocs mkdocs-material

# Navigate to project directory
cd my_site_v1
```

### Development
```bash
# Serve site locally
mkdocs serve

# Site will be available at http://localhost:8000
```

### Build
```bash
# Build static site
mkdocs build

# Output will be in 'site/' directory
```

### Update Content

#### Adding a New Blog Post
1. Create file in `docs/blog/` with format: `YYYY-MM-DD-title.md`
2. Add frontmatter with metadata:
   ```markdown
   # Title
   **Published:** Date  
   **Category:** Category Name  
   **Tags:** #tag1 #tag2
   ```
3. Update `docs/blog/index.md` with link to new post
4. Update corresponding category file in `docs/blog/categories/`
5. Update `docs/blog/archive/YYYY.md` for the year

#### Adding a New Project
1. Create file in `docs/projects/` with slug name (e.g., `my-project.md`)
2. Follow the structure in existing project files
3. Update `docs/project.md` with project card

#### Updating Profile Photo
1. Replace `docs/images/profile-placeholder.svg` with your image
2. Supported formats: PNG, JPG, SVG, WebP
3. Recommended size: 200x200px or larger
4. Reference is in `overrides/main.html`

#### Updating Navigation
- Edit the `nav:` section in `mkdocs.yml`
- Changes automatically appear in sidebar and top tabs
- Use emoji before titles for visual appeal

## 📝 Best Practices

### Code Style
- **Pythonic**: All configurations follow Python/YAML best practices
- **DRY**: No duplication of navigation or content structure
- **Maintainable**: Clear comments and organized file structure
- **Scalable**: Easy to add new sections or pages

### Content Organization
- ✅ All images in dedicated `images/` folder
- ✅ Blog posts date-named for chronological sorting
- ✅ Categories and tags for content discoverability
- ✅ Clear file hierarchy matching nav structure

### Version Control
- `.gitignore` recommended:
  ```
  site/
  .DS_Store
  __pycache__/
  *.pyc
  venv/
  ```

## 🌐 Deployment

### Static Site Hosting
The built site (in `site/` directory) can be deployed to:
- **GitHub Pages** - Free hosting with GitHub
- **Netlify** - Drag-and-drop or CI/CD
- **Vercel** - Optimized for static sites
- **AWS S3 + CloudFront** - Enterprise solution

### MkDocs Serve
For local testing:
```bash
mkdocs serve
# Access at http://localhost:8000
```

## 📦 Dependencies

```
mkdocs>=1.5.0
mkdocs-material>=9.0.0
```

## 🎯 Customization Guide

### Colors
Edit the `theme.palette` section in `mkdocs.yml`:
```yaml
palette:
  - scheme: default
    primary: blue grey      # Change primary color
    accent: cyan           # Change accent color
```

### Fonts
Add to `extra_css` in `mkdocs.yml`:
```yaml
extra_css:
  - https://fonts.googleapis.com/css?family=Roboto:300,400,700
```

### Profile Info
Edit `overrides/main.html`:
- Line 12: Update name
- Line 13: Update title/tagline
- Line 14: Update emoji/bio line

### Styling
Modify `docs/css/custom.css`:
- Profile photo styling
- Project cards
- Blog tags
- Responsive breakpoints
- Dark mode variables

## 📊 File Naming Conventions

- **Pages**: `lowercase-with-hyphens.md`
- **Blog posts**: `YYYY-MM-DD-title.md`
- **Images**: `descriptive-name.ext`
- **Folders**: `lowercase-plural`

## 🔍 SEO & Meta

Update these in `mkdocs.yml`:
- `site_name`: Website title
- `site_description`: Meta description
- `site_author`: Author name
- `site_url`: Full site URL (for sitemaps)

## 🆘 Troubleshooting

### Profile photo not showing?
- Check path in `overrides/main.html`
- Verify image file exists in `docs/images/`
- Ensure image format is supported

### Navigation not showing custom CSS?
- Run `mkdocs serve` (not `serve`)
- Clear browser cache or hard refresh
- Check CSS syntax in `docs/css/custom.css`

### Build fails?
- Verify YAML syntax in `mkdocs.yml`
- Check for broken internal links
- Ensure all referenced files exist

## 📞 Support

For issues with:
- **MkDocs**: https://www.mkdocs.org/
- **Material Theme**: https://squidfunk.github.io/mkdocs-material/
- **Markdown**: https://www.markdownguide.org/

---

**Created with ❤️**  
Last Updated: March 21, 2026
