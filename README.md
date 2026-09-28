# Content People website

Static HTML site. No build step or server-side code is required.

## Structure

```
content-people-site/
├── index.html              Opening screen / gateway (site root)
├── home.html               Homepage: full company overview
├── capital-strategy.html   Money & Strategy
├── technology.html         Tech & Architecture (includes portfolio)
├── branding-media.html     Branding & Content (includes portfolio)
├── contact.html            Contact & strategic consultation form
└── assets/images/
    ├── logo.png
    ├── favicon.png
    └── apple-touch-icon.png
```

## Deploying

Upload the whole folder to the web root (e.g. `public_html/`). All links are relative, so it also works from a sub-folder.
Visitors land on the gateway (`index.html`). The logo and "Home" menu item on inner pages open `home.html`; "Find your service" in the footer returns to the gateway.

## Before launch

1. **Contact form:** `contact.html` validates and shows a confirmation but does not send data yet. Search for `DEVELOPER NOTE` in the script and post the form to your CRM or email service.
2. **Portfolio images and client logos:** still loaded from `https://content-people-web.vercel.app/`. Download them into `assets/images/portfolio/` and `assets/images/clients/`, then update the `BASE` constant in `technology.html` and `branding-media.html` and the logo URLs in `index.html`.
3. **KSA office:** address, phone and email are placeholders in `contact.html` and every footer.
4. **Logo:** replace `assets/images/logo.png` with an SVG or 2x PNG for sharper display on high-resolution screens.
