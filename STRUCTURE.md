# Project Structure Guide

## Current Organization

```
website/
├── .github/workflows/      # GitHub Actions
├── assets/                 # Static assets
│   ├── css/               # Stylesheets
│   ├── js/                # JavaScript
│   ├── images/            # Images organized by type
│   └── fonts/             # Custom fonts
├── documents/             # Business documents (not deployed)
├── *.html                 # Page templates
├── _config.yml           # Jekyll configuration
├── robots.txt            # SEO crawler instructions
├── favicon.svg           # Site favicon
└── 404.html              # Custom error page
```

## File Organization Best Practices

### ✅ **Current Good Practices**
- Root-level HTML files for GitHub Pages compatibility
- Assets organized by type in `/assets/`
- Configuration files in root
- Proper SEO files (robots.txt, favicon)

### 🔄 **Potential Improvements**

#### Option 1: Enhanced Current (Recommended)
- Better asset suborganization (implemented)
- Component-based CSS organization
- Structured documentation

#### Option 2: Modern Static Site Structure
```
src/
├── pages/              # HTML templates
├── components/         # Reusable components
├── assets/            # Static assets
└── data/              # Site data files
```

#### Option 3: Framework-Based
- Next.js, Astro, or Jekyll site structure
- Component-based development
- Build process optimization

## When to Reorganize

Consider restructuring when you have:
- 10+ pages
- Multiple developers
- Complex build requirements
- Component reuse needs

## Migration Considerations

- GitHub Pages compatibility
- URL structure preservation
- SEO impact assessment
- Development workflow changes
