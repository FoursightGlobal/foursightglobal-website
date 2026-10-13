# Foursight Global website

Static marketing site for Foursight Global (www.foursightglobal.com.au). Plain HTML and CSS, no build step.

## Pages

| File | Page |
|---|---|
| `index.html` | Home |
| `technology-ai.html` | Technology & AI Solutions |
| `construction-sourcing.html` | Global Construction Product Sourcing |
| `capability-support.html` | Global Capability & Business Support |
| `contact.html` | Contact (email, phone, address) |

Shared styles are in `styles.css`. The site icon is `favicon.svg`. `sitemap.xml` and `robots.txt` help search engines find the pages.

## Editing the site

- **Text:** open the page's `.html` file and change the wording between the tags.
- **Colours and fonts:** change the values at the top of `styles.css` (the `:root` block).
- **Contact details:** they appear in each page's footer and the `contact.html` page. The LocalBusiness data is in each page's `<head>` (the `application/ld+json` block).

## Before launch

- Replace the abstract hero illustrations with photography if you have it. Add descriptive `alt` text to any photo.
- Check the phone number and address are current.

## Deployment

Hosted on Vercel from this GitHub repository. Any change committed to the `main` branch is published automatically.

## Security

- No inline scripts or event handlers. JavaScript lives in `js/`.
- `vercel.json` sets the security headers for every page: a Content Security Policy, HSTS, anti-clickjacking (`frame-ancestors` and `X-Frame-Options`), `nosniff`, a referrer policy and a permissions policy.
- Only Google Fonts is loaded from outside the site. The CSP allows just that origin.
- There is no form, login, or database, so there is no user data to store.
- Keep `vercel.json` in the repository root. Without it, the headers are not sent.