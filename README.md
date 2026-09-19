# Purr & Home — website files

This is the full website for Purr & Home, ready to publish on GitHub Pages with your domain (purrandhome.co.uk).

## What's in here
- `index.html`, `services.html`, `prices.html`, `areas.html`, `about.html`, `faq.html`, `book.html` — the main pages
- `blog/` — the blog, with three starter posts
- `css/`, `js/` — styling and the small bits of interactivity (mobile menu, FAQ accordion)
- `404.html` — shown if someone visits a broken link
- `CNAME`, `robots.txt`, `sitemap.xml` — technical files search engines and GitHub Pages use; you shouldn't need to touch these
- `CLAUDE.md` — a brief for Claude Code, so a future session knows your brand and site structure without you re-explaining it

## Before you go live — three things to check

1. **The "Fully insured & DBS-checked" line.** It's in the footer of every page and on the homepage. Only keep it if it's actually true — customers will take it at face value. If it isn't true yet, either sort it out first or edit it out (search for "insured" across the files).

2. **The booking form.** Right now, submitting the form on the Book page goes nowhere. To fix it:
   - Sign up free at [formspree.io](https://formspree.io)
   - Create a form and copy the form ID they give you
   - Open `book.html`, find `YOUR_FORM_ID`, and replace it with your real ID

3. **The About page bio and the "How do I pay?" answer.** Both have a short comment marking where your own words should go — open `about.html` and `faq.html` and search for "TODO" to find them.

## How to publish it

1. Create a free account at [github.com](https://github.com) if you haven't already.
2. Create a new **public** repository (Settings → your name → repositories → New).
3. Upload every file and folder in here, keeping the same structure (drag the whole lot into GitHub's "Add file → Upload files" screen — it preserves folders).
4. In the repository's **Settings → Pages**, set it to publish from the `main` branch.
5. Still in Settings → Pages, add your custom domain: `purrandhome.co.uk`.
6. At your domain registrar, add the DNS records GitHub shows you (usually four A records for the root domain, plus a CNAME record for `www`).
7. Wait for DNS to update (a few minutes to a few hours), then tick **Enforce HTTPS** in the Pages settings.

Once it's live, submit the site to [Google Search Console](https://search.google.com/search-console) and submit `sitemap.xml` so Google finds it quickly.

## Making changes later

For small text edits, you can edit files directly on GitHub's website (click a file, then the pencil icon). For anything bigger — new pages, redesigns, more blog posts — point Claude Code at this repository and it can make the changes for you.
