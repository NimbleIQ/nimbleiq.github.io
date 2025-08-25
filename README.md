# NimbleIQ Website

Professional marketing science consulting website for NimbleIQ, featuring modern design, responsive layout, and automated deployment.

## Overview

NimbleIQ is a senior-level marketing science boutique focused on turning noisy data into confident budget decisions. We specialize in:

- Media Mix Modeling (MMM)
- Event & Campaign Measurement
- Customer Segmentation
- Decision Science & Analytics

## Website Features

- **Modern, Responsive Design**: Mobile-first approach with excellent UX
- **Fast Loading**: Optimized performance with minimal dependencies
- **SEO Optimized**: Schema markup, meta tags, and semantic HTML
- **Automated Deployment**: GitHub Actions workflow for seamless updates
- **Professional Color Palette**: Easily configurable design tokens
- **Accessible**: WCAG-compliant design and markup

## Technology Stack

- **Frontend**: HTML5, CSS3 (with CSS Custom Properties), Vanilla JavaScript
- **Hosting**: GitHub Pages
- **Deployment**: GitHub Actions
- **Typography**: Roboto (Google Fonts)
- **Design System**: CSS Custom Properties for consistent theming

## Local Development

1. Clone the repository:
   ```bash
   git clone git@github.com:NimbleIQ/website.git
   cd website
   ```

2. Use a local development server:
   ```bash
   # Recommended: Python (handles Jekyll permalinks correctly)
   python3 -m http.server 8000
   
   # Alternative: Node.js live-server (with hot reload)
   npm install -g live-server
   live-server --port=8000
   
   # Alternative: PHP
   php -S localhost:8000
   
   # Note: Avoid basic 'npx serve' as it may cause asset path issues
   ```

3. Visit `http://localhost:8000` to view the site

## Deployment

The website automatically deploys to GitHub Pages when changes are pushed to the `main` branch. The deployment workflow:

1. Triggers on push to `main`
2. Builds the site using Jekyll
3. Deploys to GitHub Pages
4. Available at: `https://nimbleiq.github.io/website`

## Project Structure

```
website/
├── index.html             # Homepage
├── services.html          # Services page
├── about.html             # About page
├── case-studies.html      # Case studies page
├── contact.html           # Contact page
├── assets/
│   ├── css/
│   │   └── styles.css     # Main stylesheet
│   ├── js/
│   │   └── main.js        # Main JavaScript
│   └── images/            # Image assets
├── documents/             # Business planning documents
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Actions deployment
└── README.md             # This file
```

## Content Management

### Adding New Pages

1. Create new HTML file in root directory
2. Follow the existing template structure
3. Update navigation in all pages
4. Add appropriate meta tags and schema markup

### Updating Styles

All styles are in `assets/css/styles.css` using CSS Custom Properties for easy theming:

```css
:root {
  --primary-color: #2563eb;    /* Change primary color */
  --accent-color: #10b981;     /* Change accent color */
  /* ... other design tokens */
}
```

### Lead Generation Integration

The contact forms are currently set up with placeholder functionality. To integrate with real services:

1. **Calendly**: Replace placeholder functions in `contact.html` with actual Calendly embed
2. **Email Marketing**: Update form handlers in `main.js` to integrate with your email service
3. **Analytics**: Add Google Analytics or similar tracking code

## Performance Optimizations

- Minimal external dependencies
- Optimized images and fonts
- Efficient CSS with custom properties
- Compressed and minified assets in production
- Proper caching headers via GitHub Pages

## SEO Features

- Semantic HTML structure
- Schema.org markup for better search understanding
- Optimized meta descriptions and titles
- Fast loading times
- Mobile-responsive design
- Clean URL structure

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Contributing

1. Create a feature branch from `main`
2. Make your changes
3. Test thoroughly across devices and browsers
4. Create a pull request with detailed description
5. Merge after review and testing

## Troubleshooting

### Common Development Issues

**Asset Loading (404 errors on CSS/JS):**
- ✅ Use `python3 -m http.server 8000` for development
- ❌ Avoid `npx serve` which can cause URL redirect issues
- All asset paths are absolute (`/assets/...`) for consistency

**Jekyll Permalink Issues:**
- Production site uses `permalink: pretty` (removes .html extensions)
- Python server handles this correctly
- Live site: https://nimbleiq.github.io

**Favicon Not Loading:**
- Favicon is at `/assets/images/icons/favicon.svg`
- Uses absolute path for cross-browser compatibility
- Clear browser cache if not updating

### Development vs Production

| Environment | URL Structure | Asset Paths |
|-------------|---------------|-------------|
| **Local** | `localhost:8000/contact.html` | `/assets/css/styles.css` |
| **Production** | `nimbleiq.github.io/contact` | `/assets/css/styles.css` |

Both environments use **absolute asset paths** for consistency.

## Support

For questions or issues with the website, please contact the development team or create an issue in this repository.

## License

© 2024 NimbleIQ. All rights reserved.
