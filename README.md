# oceans.computer

The Oceans studio website. Plain HTML, CSS and SVG. No JavaScript, frameworks, package dependencies, external fonts, tracking, or build step.

## Files

- `public/index.html` — content, metadata, and decorative wave paths
- `public/styles.css` — layout and CSS wave animations, including reduced-motion support
- `public/assets/` — logo, favicon, and social preview image
- `vercel.json` — static hosting configuration

## Preview locally

From the repository root:

```sh
python3 -m http.server 4173 --directory public
```

Open http://localhost:4173. Python is only a convenient local server; it is not needed for deployment.

## Deploy with Vercel

1. Import this GitHub repository into Vercel.
2. Keep the root directory at the repository root. The included `vercel.json` selects **Other**, skips installation and building, and serves `public/`.
3. Deploy, then add `oceans.computer` under the project's domain settings and apply the DNS records Vercel provides.

The files in `public/` can also be served directly by any static web host.

## Editing

Edit the HTML or CSS directly and push to the connected branch. The approved original wave curves, spacing, and drift speeds are retained, with a subtle four-unit swell. Visitors can pause all waves using the CSS-only checkbox in the footer. All animation stops automatically when reduced motion is preferred, and the redundant pause control is hidden.

In forced-colour/high-contrast mode, the decorative waves and fixed-colour logo image are hidden; the Oceans wordmark and content use the visitor's system colours.

## Deployment headers

`vercel.json` sets a Content Security Policy that permits only local images and styles, disables MIME sniffing, and omits outgoing referrer information. Adding scripts, forms, third-party assets, or embedded content requires reviewing this policy. Other static hosts should apply the same headers in their own configuration.
