# Icons Directory

## Current Icons
- `favicon.svg` - Main site favicon (scalable vector)

## Future Icon Assets
When you need additional favicons for better compatibility:

- `favicon-16x16.png` - 16x16 pixel favicon
- `favicon-32x32.png` - 32x32 pixel favicon  
- `apple-touch-icon.png` - 180x180 for iOS devices
- `android-chrome-192x192.png` - 192x192 for Android
- `android-chrome-512x512.png` - 512x512 for Android

## Favicon Generation
Use tools like:
- https://realfavicongenerator.net/
- https://favicon.io/
- Adobe Illustrator or Figma export

## HTML Implementation
Current implementation uses SVG favicon which works in all modern browsers.
For maximum compatibility, add PNG fallbacks:

```html
<!-- Modern browsers -->
<link rel="icon" href="assets/images/icons/favicon.svg" type="image/svg+xml">
<!-- Fallback for older browsers -->
<link rel="icon" href="assets/images/icons/favicon-32x32.png" type="image/png" sizes="32x32">
<link rel="icon" href="assets/images/icons/favicon-16x16.png" type="image/png" sizes="16x16">
<!-- Apple devices -->
<link rel="apple-touch-icon" href="assets/images/icons/apple-touch-icon.png">
```
