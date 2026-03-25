# Deployment Guide — ryanwang.cc

## Option 1: Cloudflare Pages (Recommended)

Cloudflare owns the DNS for ryanwang.cc, so this is the simplest path.

### Steps
1. Push this directory to a GitHub repo (e.g., `ryanwang.cc`)
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/) > Pages > Create a project
3. Connect your GitHub repo
4. Build settings: **no build command needed**, output directory: `/` (root)
5. Deploy
6. In Cloudflare DNS, add a CNAME record: `ryanwang.cc` → `<your-project>.pages.dev`
7. Cloudflare will auto-provision SSL

### Custom domain
- In Pages project settings > Custom domains > Add `ryanwang.cc`
- Cloudflare handles SSL and CDN automatically

## Option 2: Vercel

1. Push to GitHub
2. Import in [Vercel](https://vercel.com/new)
3. Framework preset: **Other** (static)
4. Deploy
5. Add custom domain `ryanwang.cc` in project settings
6. Update DNS: CNAME `ryanwang.cc` → `cname.vercel-dns.com`

## Option 3: Netlify

1. Push to GitHub
2. Import in [Netlify](https://app.netlify.com/)
3. No build command, publish directory: `/`
4. Add custom domain, update DNS

## File Structure

```
/
├── index.html          # Main landing page (all sections)
├── blog/
│   ├── index.html      # Blog listing page
│   └── _template.html  # Template for new blog posts
└── DEPLOY.md           # This file
```

## Adding Blog Posts

1. Copy `blog/_template.html` to `blog/your-post-slug.html`
2. Replace `POST_TITLE`, `POST_DATE`, `POST_DESCRIPTION` placeholders
3. Write your content in the article body
4. Add an entry to `blog/index.html` in the posts list (see HTML comment in that file)
5. Commit and push — auto-deploys

## DNS Notes

If the domain is on Cloudflare:
- Use **proxied** CNAME (orange cloud) for Cloudflare Pages
- Use **DNS only** CNAME (gray cloud) for Vercel/Netlify (they handle SSL)
