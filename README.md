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
└── assets/images/          logo.png, favicon.png, apple-touch-icon.png
```

Each page is self-contained: its styles and scripts are inside the HTML file.
The only shared files are the images in `assets/images/`, which must be uploaded with the pages.

Colours are defined at the top of each page's `<style>` block (`--navy`, `--blue`, etc.).

## Deploying

Upload the contents of this folder to the web root, or connect the repository to Vercel
(Framework Preset: Other, no build command). All links are relative.

Visitors land on the gateway (`index.html`). The logo and "Home" menu item on inner pages
open `home.html`; "Find your service" in the footer returns to the gateway.

## Before launch

1. **Contact form:** `contact.html` validates and shows a confirmation but does not send data yet.
   Search for `DEVELOPER NOTE` and post the form to your CRM or email service.
2. **Portfolio images and client logos:** still loaded from `https://content-people-web.vercel.app/`.
   Download them into `assets/images/portfolio/` and `assets/images/clients/`, then update the `base`
   value in the `window.PORTFOLIO` block of `technology.html` and `branding-media.html`, the
   "Recently delivered" images in `home.html`, and the client logo URLs in `home.html`.
3. **Logo:** replace the logo PNGs with SVG or 2x versions for sharper display on high-resolution screens.
4. **Figures and new copy:** confirm the homepage key figures (65+ projects, 8+ countries) and the
   "How an engagement works" stages with the client.

## Contact details

Office address, phone numbers, WhatsApp and email appear in the footer of every page,
in the contact panel on `contact.html`, and in the bottom bar of `index.html`.
Update all three places if they change.
