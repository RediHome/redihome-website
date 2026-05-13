# RediHome — 57th Street Collection

Static landing page for redihome.io.

## Deploy to Vercel

### Option 1 — Drag & Drop (fastest)
1. Go to https://vercel.com/new
2. Drag the `public/` folder into the upload area
3. Click Deploy
4. Done — Vercel gives you a live URL

### Option 2 — Vercel CLI
```bash
npm i -g vercel
cd redihome-site
vercel
```

### Option 3 — Connect a Git repo
1. Push this folder to GitHub
2. Import the repo in Vercel
3. Set output directory to `public`
4. Deploy

## File Structure
```
redihome-site/
├── public/
│   ├── index.html       ← the page
│   ├── styles.css       ← all styling
│   └── images/
│       ├── lineup.jpg
│       ├── tuggle-kitchen.jpg
│       ├── tuggle-living.jpg
│       ├── powell-entry.jpg
│       ├── powell-living.jpg
│       ├── pettiford-flat.jpg
│       └── pettiford-vaulted.jpg
└── vercel.json          ← cache config
```

## Before You Go Live — Edit These Two Things

### 1. Formspree form ID (line ~125 of index.html)
The form currently posts to `https://formspree.io/f/YOUR_FORM_ID`.

- Sign up at https://formspree.io (free tier handles 50 submissions/mo)
- Create a new form, copy your form ID
- Replace `YOUR_FORM_ID` in index.html

### 2. Contact email (line ~138 of index.html)
Currently set to `sales@redihome.io` — confirm this is the right inbox.

## Editing Content

All content lives in `public/index.html`. Plain HTML — no build step, no React, no dependencies.

To swap a rendering, drop the new JPG into `public/images/` with the same filename.

To update a plan description, find the matching `<article class="plan">` block and edit the text.

## When the Rickwood Renderings Arrive

Find this block in `index.html`:

```html
<div class="plan-image plan-image-placeholder">
  <div class="placeholder-content">...</div>
  <span class="status">Coming Soon</span>
</div>
```

Replace with:

```html
<div class="plan-image">
  <img src="/images/rickwood-hero.jpg" alt="The Rickwood" loading="lazy" />
  <span class="status">Coming Soon</span>
</div>
```

## When 141 57th Is Photographable

The single biggest upgrade you can make: swap the hero `lineup.jpg` for real architectural photography of the finished Tuggle. Everything else stays the same.
