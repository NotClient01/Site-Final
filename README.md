# New Horizon Precision - Drone Services Website

A modern, responsive website for New Horizon Precision, offering advanced agricultural and land management drone services across East Tennessee and the South.

## Features

- **Responsive Design**: Mobile-first approach with modern CSS Grid and Flexbox
- **Performance Optimized**: Lazy loading images, optimized assets, and efficient CSS
- **SEO Ready**: Meta tags, Open Graph, Twitter Cards, sitemap, and robots.txt
- **Production Ready**: Clean asset structure, proper paths, and deployment configurations

## Local Development

### Quick Start
Simply open `index.html` in your browser, or use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have npx)
npx serve .

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000`

### Project Structure
```
/
├── index.html              # Main homepage
├── about.html              # About page
├── reference.html          # Reference version of homepage
├── assets/
│   ├── css/
│   │   └── styles.css      # Main stylesheet
│   ├── js/
│   │   └── main.js         # JavaScript functionality
│   └── img/                # All images (kebab-case naming)
├── .github/workflows/      # CI/CD workflows
├── robots.txt              # SEO robots file
├── sitemap.xml             # SEO sitemap
└── do-app.yaml            # DigitalOcean App Platform config
```

## Deployment

### GitHub Pages
1. Push your code to GitHub
2. Go to repository Settings → Pages
3. Select "Deploy from a branch"
4. Choose `main` branch and `/` folder
5. Enable GitHub Pages in repository variables:
   - Go to Settings → Secrets and variables → Actions
   - Add repository variable: `USE_GITHUB_PAGES` = `true`

### DigitalOcean App Platform

#### Option 1: Using the Dashboard
1. Go to [DigitalOcean App Platform](https://cloud.digitalocean.com/apps)
2. Click "Create App"
3. Connect your GitHub repository
4. Select the repository and branch
5. Choose "Static Site" as the environment
6. Set source directory to `/`
7. Deploy

#### Option 2: Using the App Spec
1. Ensure your repository is connected to DigitalOcean
2. Use the provided `do-app.yaml` configuration
3. Deploy via dashboard or CLI

### DNS Configuration (Namecheap → DigitalOcean)

#### For www subdomain:
1. In Namecheap DNS settings, add a CNAME record:
   - Host: `www`
   - Value: `[your-app-name].ondigitalocean.app`
   - TTL: Automatic

#### For apex domain (@):
1. In Namecheap DNS settings, add an A record:
   - Host: `@`
   - Value: `[DigitalOcean IP addresses]` (provided in App Platform)
   - TTL: Automatic

2. Or if Namecheap supports ALIAS/ANAME:
   - Host: `@`
   - Value: `[your-app-name].ondigitalocean.app`
   - TTL: Automatic

### HTTPS Configuration
- DigitalOcean App Platform automatically provides SSL certificates
- Ensure all internal links use relative paths (starting with `/`)
- No mixed content (http/https) issues

## Quality Assurance

### Automated Checks
The GitHub Actions workflow automatically:
- Checks for forbidden local paths (`file:///`, `\Users\`, etc.)
- Validates all links using Lychee
- Ensures no mixed content issues

### Manual Testing
1. **Cross-browser testing**: Chrome, Firefox, Safari, Edge
2. **Mobile responsiveness**: Test on various screen sizes
3. **Performance**: Use Lighthouse for performance audits
4. **Accessibility**: Check with screen readers and keyboard navigation

## Customization

### Colors
The site uses CSS custom properties for easy theming:
```css
:root {
    --color-dark-green: #1E3D2F;
    --color-golden-yellow: #E4A936;
    --color-off-white: #F6F2EA;
    /* ... more colors */
}
```

### Fonts
The site uses Clarendon font family. To change:
1. Update the `font-family` properties in `assets/css/styles.css`
2. Ensure the new font is available or include it via Google Fonts

### Images
- All images are in `assets/img/` with kebab-case naming
- Use root-relative paths: `/assets/img/filename.jpg`
- Add `loading="lazy"` for non-critical images

## Maintenance

### Regular Tasks
1. **Update dependencies**: Check for security updates
2. **Performance monitoring**: Regular Lighthouse audits
3. **Content updates**: Keep service information current
4. **SEO monitoring**: Check search console for issues

### Troubleshooting
- **Images not loading**: Check file paths and case sensitivity
- **CSS not applying**: Verify the stylesheet is linked correctly
- **Deployment issues**: Check GitHub Actions logs for errors

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Contact

For technical support or questions about this website:
- Email: info@newhorizonprecision.com
- Website: https://newhorizonprecision.com

---

**Built with modern web standards and optimized for performance.**

