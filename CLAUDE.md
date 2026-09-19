# Purr & Home — site brief

Static HTML/CSS/JS site for a self-employed cat sitting business in Chorley, Lancashire. No build step — plain files served as-is by GitHub Pages. Deployed at https://purrandhome.co.uk (custom domain set via the `CNAME` file).

## Brand
- Name: Purr & Home
- Owner: Charli
- Service: cat sitting / pet visiting, based in Chorley, covering Euxton, Buckshaw Village, Astley Village, Adlington, Coppull, Clayton-le-Woods, Whittle-le-Woods and nearby areas
- Tone: warm, calm, reassuring, plain-spoken — never salesy or corporate
- Contact used throughout: purrandhome@gmail.com · 07464 845362

## Palette (defined in css/style.css :root)
- Cream `#FAF5EC` — background
- Forest `#2F4A42` — primary/headings/nav/buttons
- Sage `#9DB39A` / sage-light `#E4EBE3` — secondary sections
- Apricot `#E8985E` — accent (ginger-cat nod)
- Butter `#F4D58D` — small highlights
- Charcoal `#2E2B29` — body text

## Type
Fraunces (headings, via Google Fonts) + Karla (body/UI), loaded in css/style.css.

## Structure
- `/index.html` — home
- `/services.html`, `/prices.html`, `/areas.html`, `/about.html`, `/faq.html`, `/book.html`
- `/blog/index.html` + one file per post (`/blog/<slug>.html`)
- `/css/style.css`, `/js/main.js` (mobile nav toggle + FAQ accordion)
- `/404.html`, `/robots.txt`, `/sitemap.xml`, `/CNAME`
- No templating: header/nav and footer markup is duplicated at the top/bottom of every page. When editing shared markup (nav links, footer, brand mark), update it in every file — grep for the string first.
- All internal links and asset paths are root-relative (`/css/style.css`, `/services.html`) so they work at any folder depth, including inside `/blog/`.

## SEO conventions already in place
- Every page has a unique `<title>`, meta description, and `<link rel="canonical">` pointing at `https://purrandhome.co.uk/...`.
- Home page and FAQ page carry JSON-LD structured data (`LocalBusiness` and `FAQPage`).
- Local keywords ("cat sitting in Chorley", named surrounding areas) are used naturally in headings and body copy — don't keyword-stuff.
- `sitemap.xml` must be updated whenever a new page is added.

## Known placeholders — check before/soon after publishing
- **Enquiry form** (`book.html`): posts to Formspree with a placeholder form ID (`YOUR_FORM_ID`). Needs a real Formspree (or equivalent) form ID before it will deliver submissions.
- **Calendar embed** (`book.html`): currently a static placeholder box. Swap for a real Calendly (or similar) `<iframe>` embed when set up.
- **About page bio**: has an HTML comment marking where Charli's own story should go — currently no invented biographical claims.
- **"Fully insured & DBS-checked"**: appears in every footer and in the homepage hero trust line. This is a factual claim customers will rely on — only keep it if true; otherwise remove or amend before the site goes live.
- **FAQ "How do I pay?"**: answer left blank as an HTML comment for Charli to fill in.
- **Testimonial quote** on the homepage is illustrative placeholder copy, not a real review — replace with an actual client quote (with permission) before publishing, or remove the section.

## Adding a blog post
1. Copy an existing file in `/blog/` as a starting point.
2. Update `<title>`, meta description, canonical URL, `<h1>`, post date, and body content.
3. Add a new `<article class="post-card">` entry to `/blog/index.html`.
4. Add the new URL to `/sitemap.xml`.
