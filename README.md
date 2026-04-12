# Mithu Surendra — Website

**Live site:** `https://[yourusername].github.io/mithu-surendra`  
**Build phase:** Phase 4 — Initial Build Complete  
**Last updated:** April 2026

---

## What this is

The production website for Mithu Surendra — spiritual healer, author, and guide. Built as a single self-contained HTML file for GitHub Pages hosting. No frameworks, no dependencies, no build process required. Open the file, push it, it works.

The site functions as a conversion funnel: it earns trust through story, explains the methodology, provides social proof through testimonials, and directs visitors toward one of three actions — the somatic self-diagnosis (free), the Self-Love School ($50/month), or a 1-on-1 discovery call (free).

---

## Repository contents

```
index.html                      — The complete website (single file)
Profile_Pic.jpg                 — Hero image (event, warm ambient light)
Profile_Pic_-_Professional.jpg  — Story section top photo (blue blazer, night)
IMG_1897.jpg                    — Story section bottom photo (Bali scooter)
IMG_1899.jpg                    — Book section (seated with book, yoga mat)
Workshop.PNG                    — Method section (mic, raised arm, Bali venue)
Pranava_1.JPEG                  — School section (Pranava Yoga community shot)
README.md                       — This file
```

All image files must live in the same directory as `index.html`. The HTML references them by filename only — no subfolders, no paths.

---

## Sections — what's built

| Section | Status | Notes |
|---|---|---|
| Navigation | ✅ Complete | Fixed, solidifies on scroll, hamburger on mobile |
| Hero | ✅ Complete | Profile_Pic.jpg full-bleed left, copy right, parallax |
| Story | ✅ Complete | Two-column sticky photo stack, first-person copy |
| The Lion Work | ✅ Complete | Workshop.PNG with badge overlay, 4 phase rows |
| Transformation | ✅ Complete | Before/after grid, sourced from ICP document |
| Testimonials | ✅ Complete | Emanuele featured full-width, 6-card grid |
| Somatic Diagnosis | ⏳ Placeholder | Embed slot built — awaiting external tool |
| Self-Love School | ✅ Complete | Pranava_1.JPEG, discernment copy, pricing card |
| Coaching | ✅ Complete | Discovery Call featured, 1-on-1 second, booking link live |
| The Book | ✅ Complete | IMG_1899.jpg, copy live, purchase link pending |
| Email Capture | ⏳ Placeholder | Form built — awaiting Mailchimp integration |
| Footer | ✅ Complete | Logo, tagline, nav links, Instagram |

---

## What still needs to be connected

### 1. Somatic Self-Diagnosis embed
The section is built and styled. When the external tool is ready (Typeform, Tally, or equivalent), paste the embed code inside this element in `index.html`:

```html
<div class="diagnosis-embed">
  <!-- paste embed code here -->
</div>
```

Remove the placeholder text inside that div before adding the embed.

### 2. Mailchimp email form
The form UI is built. To connect it to Mailchimp:
1. Create a Mailchimp audience if you haven't already
2. Go to Audience → Signup forms → Embedded forms → copy the form `action` URL
3. In `index.html`, find the `.email-form` element and add:
   - `action="[your mailchimp url]"` to the form
   - `method="POST"` to the form
   - Change `<div class="email-form">` to `<form class="email-form" ...>`
   - Change `<button type="button">` to `<button type="submit">`

### 3. Book purchase link
When the book is available to purchase, find this line in `index.html`:

```html
<span class="coming reveal rd2">Purchase link coming soon</span>
```

Replace with:

```html
<a href="[book url]" target="_blank" rel="noopener" class="cta-ghost">Get the Book →</a>
```

### 4. og:image for social sharing
Once a custom domain is live, update this meta tag in `index.html`:

```html
<meta property="og:image" content="Profile_Pic.jpg">
```

Replace with the full URL:

```html
<meta property="og:image" content="https://[yourdomain.com]/Profile_Pic.jpg">
```

---

## Custom domain (when ready)

1. Purchase domain (recommended: `mithusurendra.com`)
2. In GitHub repo → Settings → Pages → Custom domain → enter domain
3. At your domain registrar, add a CNAME record pointing to `[yourusername].github.io`
4. GitHub will provision HTTPS automatically within 24 hours
5. Update the `og:image` meta tag as noted above

---

## Design system — quick reference

If making copy or style edits, the site uses:

| Element | Value |
|---|---|
| Background | `#0c0f0a` (green-tinted black) |
| Text | `#f0e8d0` (warm off-white) |
| Gold accent | `#c9920a` / `#e8a820` |
| Ember CTA | `#d4560a` |
| Display font | Fraunces (serif, italic for emphasis) |
| Handwritten label | Caveat |
| Body font | DM Sans |
| Mono / eyebrow | Space Mono |

All CSS tokens are defined as variables at the top of `index.html` inside `:root {}`. Edit there first — changes cascade through the whole site.

---

## Copy rules — do not drift from these

All copy on this site was sourced from Mithu's interview transcripts. Before editing any copy:

- Write in first person — "I", "my", "me" — never third person
- Lead with pain before aspiration
- Use active, declarative language — "I chose", "I decided", "I walked away"
- Do not sanitise or soften — the rawness is the authority
- Direct quotes must come from transcripts only

The internal documentation repository contains the full copy brief, ICP, story extraction, and testimonial reference documents.

---

## Phase 5 — what comes next

- [ ] Somatic self-diagnosis tool built and embedded
- [ ] Mailchimp audience created and form connected
- [ ] Welcome email sequence written and loaded (5-part)
- [ ] Custom domain purchased and pointed
- [ ] Instagram link-in-bio updated to point to site
- [ ] Book purchase link added when available
- [ ] Analytics added (Plausible or Google Analytics)
- [ ] Review conversion data after 30 days — optimise

---

*Internal documentation for this project lives in a separate private repository. Do not add internal documents to this repository.*
