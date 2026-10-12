# isindemo.com

Landing page for the bare `isindemo.com` domain. Client previews live on subdomains (`client1.isindemo.com`); this is what people see when they leave the subdomain off.

The address bar on the page works: type a subdomain, press Enter, and it goes to `https://<subdomain>.isindemo.com/`.

It is a single static page: `index.html` (markup, styles and script inline) plus `favicon.svg`. No dependencies, no build step. The only external request is the Fraunces webfont from Google Fonts.

## Run locally

```bash
python3 -m http.server 4173
```

Then open http://localhost:4173.

## Deploy to Vercel

Import this repo in Vercel and accept the defaults: framework preset "Other", no build command, output directory left empty. Vercel serves the repo root as static files. Then add `isindemo.com` as the project's domain.

Or from this folder:

```bash
vercel --prod
```

## Editing the jokes

Everything the janitor says is at the top of the `<script>` in `index.html`:

- `CAUGHT`: what he says when the spotlight lands on him, in order.
- `NOPE`: what he says when you find him hiding behind a curtain.
- `ANSWERS`: his replies to the "Why are you here?" buttons.
- `ADDRESS`: what he says when the address bar is submitted (empty, `www`, or on the way out).
