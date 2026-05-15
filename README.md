# Jeff Carley Leadership — Resource Pages
## Hosted on Netlify | Connected to GitHub

This repo contains the standalone resource pages for jeffcarleyleadership.com.
These pages live here because the main WordPress.com site (free plan) cannot
serve custom sub-pages. Netlify handles routing and deployment automatically.

---

## Live URLs (after deployment)

| Page | URL |
|------|-----|
| Climb Map (email gate) | `your-netlify-url.netlify.app/climb-map` |
| 5 Questions (free resource) | `your-netlify-url.netlify.app/5-questions` |
| Thank You / Download | `your-netlify-url.netlify.app/thank-you` |

If you set up a custom subdomain (recommended):
- `resources.jeffcarleyleadership.com/climb-map`
- `resources.jeffcarleyleadership.com/5-questions`

---

## File Structure

```
jeffcarley-site/
├── index.html          ← redirects to jeffcarleyleadership.com
├── netlify.toml        ← routing + headers config
├── README.md           ← this file
└── pages/
    ├── climb-map.html      ← Climb Map landing page (email gate)
    ├── 5-questions.html    ← 5 Questions free resource
    └── thank-you.html      ← Download confirmation page
```

---

## Deployment (already done — auto-deploys on every push)

1. Push any change to this repo
2. Netlify detects the push automatically
3. Site rebuilds in ~10 seconds
4. Changes are live

---

## After Deployment — Update These Two Things

### 1. Update homepage resource links in WordPress theme editor
Change both resource links from WordPress slugs to your Netlify URLs:
- `/climb-map` → `https://YOUR-NETLIFY-URL.netlify.app/climb-map`
- `/5-questions` → `https://YOUR-NETLIFY-URL.netlify.app/5-questions`

### 2. Update MailPoet form redirect
In MailPoet → Forms → your Climb Map form → After submission:
- Change redirect URL to: `https://YOUR-NETLIFY-URL.netlify.app/thank-you`

---

## Custom Domain (optional but recommended)

To use `resources.jeffcarleyleadership.com`:
1. Netlify → Site settings → Domain management → Add custom domain
2. Enter: `resources.jeffcarleyleadership.com`
3. In your domain DNS (wherever jeffcarleyleadership.com is registered):
   - Add CNAME record: `resources` → `YOUR-NETLIFY-SITE.netlify.app`
4. Wait 5–30 minutes for DNS to propagate
5. Netlify auto-provisions SSL certificate

---

## To Do (remaining items)

- [ ] Update homepage theme links to Netlify URLs
- [ ] Update MailPoet form redirect to Netlify thank-you URL  
- [ ] Set up custom subdomain (optional)
- [ ] Complete MailPoet welcome email (Screen 4)
- [ ] Build WPForms contact form and add shortcode to homepage
- [ ] Fix Speaker One-Sheet link: change to `-v2.pdf`
- [ ] Add Privacy Policy page (WP Admin → Tools → Privacy)
- [ ] Remove "1,000+ Leaders" from newsletter section (not yet accurate)
- [ ] Add real testimonials when collected
- [ ] Upgrade to WordPress.com Business plan when budget allows
  (eliminates need for this Netlify workaround entirely)
