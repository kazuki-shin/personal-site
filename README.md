# kazuki.dev

Personal website & blog.

## File structure

```
├── index.html                    ← Homepage
├── style.css                     ← Shared styles (all pages use this)
├── writing/
│   ├── why-healthcare.html
│   ├── leverage-modern-founder.html
│   └── fashion-photography-product-design.html
└── README.md
```

## How to add a new blog post

1. **Copy an existing post** — duplicate any file in `writing/` and rename it:
   ```bash
   cp writing/why-healthcare.html writing/my-new-post.html
   ```

2. **Edit the new file** — update the `<title>`, meta description, date, heading, subtitle, and body content. The structure is straightforward HTML — just replace the text.

3. **Add a link on the homepage** — open `index.html` and add a new `<li class="post-item">` block in the `<ul class="post-list">` section. Copy an existing one and update the `href`, date, title, excerpt, and tags.

4. **Push to deploy:**
   ```bash
   git add .
   git commit -m "New post: my-new-post"
   git push
   ```
   Vercel auto-deploys on push. Your post will be live in ~30 seconds.

## Photos

Replace the placeholder `<div class="photo-placeholder">` elements in `index.html` with actual images:

```html
<div class="photo-item">
  <img src="photos/nyfw-01.jpg" alt="NYFW runway shot">
</div>
```

Create a `photos/` directory and add your images there. Recommended: square crop, 800×800px or larger.

## Custom domain

In Vercel dashboard → Settings → Domains → add your domain (e.g. `kazuki.dev`). Point your domain's DNS to Vercel's nameservers. SSL is automatic.
