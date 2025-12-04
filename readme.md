# Hidden Cost Index – Complete Site

## Overview

A complete, production-ready website for **HiddenCostIndex.co.za** that quantifies the true cost of living in South Africa by measuring “hidden costs” – security, load shedding, private healthcare, transport dependency and crime risk.

## Site Structure

### Pages

1. **index.html** – Landing page
- Hero section with value proposition
- Example metrics from typical urban SA household
- Overview of the six hidden cost categories
- Clear CTAs to dashboard
1. **dashboard.html** – Interactive dashboard (3 tabs)
- **Tab 1: Explainer** – Model logic and flow diagram
- **Tab 2: Calculator** – Live calculator with user inputs
- **Tab 3: City Comparison** – Compare Johannesburg, Cape Town, Melbourne, Shenzhen
1. **methodology.html** – Technical documentation
- Core definitions and mathematical structure
- Data inputs and sources (current + planned)
- Limitations and interpretation guidelines
- Roadmap for future enhancements
1. **about.html** – About & FAQ
- Project goals and what it is/isn’t
- Frequently asked questions
- Contact information and disclaimer

## Features

### Calculator (Tab 2)

- Real-time calculation of:
  - Hidden Cost Total (R/month)
  - Shadow Tax Rate (% of gross income)
  - True Disposable Income (what’s actually left)
  - Hidden Cost Index (HCI) – ratio vs basic living costs
- Six cost categories: Security, Infrastructure, Health, Transport, Education, Crime
- Warning triggers for high-burden households

### City Comparison (Tab 3)

- Pre-configured scenarios for 4 cities
- Visual bar charts showing relative HCI
- Detailed breakdowns of net income, basic costs, hidden costs

### Design

- Dark theme optimized for readability
- Fully responsive (mobile, tablet, desktop)
- Accessible navigation and semantic HTML
- No external dependencies – pure HTML/CSS/JS

## Deployment

### Quick Deploy (Vercel/Netlify)

1. Push these files to a GitHub repo
1. Connect to Vercel or Netlify
1. Set root directory to where these HTML files are
1. Deploy – done

### Manual Deploy

```bash
# Upload all .html files to your web server
scp *.html user@hiddencostindex.co.za:/var/www/html/

# Or use FTP/SFTP client of your choice
```

### DNS Setup

Point your domain to your hosting:

```
A Record: hiddencostindex.co.za → [your server IP]
CNAME: www → hiddencostindex.co.za
```

## File Sizes

- index.html: ~14KB
- dashboard.html: ~37KB (includes all 3 tabs + JavaScript)
- methodology.html: ~13KB
- about.html: ~10KB

**Total: ~74KB** (extremely lightweight)

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- No JavaScript required for landing/static pages
- Calculator requires JavaScript

## Customization

### Update Contact Email

Replace placeholder in `about.html`:

```html
<span>info@hiddencostindex.co.za</span>
```

### Add Favicon

Place your favicon.png in the root directory (referenced in all pages)

### Update Scenarios

Edit the `scenarios` object in `dashboard.html` (around line 750) to adjust city comparison data:

```javascript
const scenarios = {
  jhb: { net: 35000, core: 20000, hidden: 11800 },
  // ... adjust values
};
```

## SEO Ready

- Meta descriptions on all pages
- Open Graph tags for social sharing
- Semantic HTML structure
- Fast load times (no external dependencies)

## Privacy

- Calculator runs entirely client-side
- No data collection or analytics (add your own if needed)
- No cookies required for core functionality

## Next Steps

1. **Before launch:**
- Add real contact email in about.html
- Create favicon.png and og-image.png
- Test all forms and calculations
- Verify mobile responsiveness
1. **After launch:**
- Set up analytics (Google Analytics, Plausible, etc.)
- Monitor user feedback via contact form
- Iterate on city comparison scenarios with real data
1. **Roadmap features:**
- Save/export calculator results
- More cities in comparison tab
- API for researchers/journalists
- Integration with live data feeds (fuel prices, CPI)

## License

All rights reserved © HiddenCostIndex.co.za

## Support

For questions or issues, contact: info@hiddencostindex.co.za

-----

**You now have a complete, professional site ready to deploy.**
Wire up DNS, push to Vercel/Netlify, and you’re live.