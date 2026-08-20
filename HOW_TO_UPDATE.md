# How to Update This Website

Live at https://shashishekhawat.github.io

The site is now plain, hand-editable HTML — no build step, no JavaScript, no framework.

```
index.html          the whole page (content + styles, ~18 KB)
robots.txt          lets search engines index the site
assets/portrait.jpg  photo shown at the top
assets/og-card.jpg   preview image for LinkedIn / WhatsApp / Slack links
assets/favicon.svg   browser tab icon
```

## Making a change

1. Open `index.html` in any text editor (or ask Claude Code to edit it).
2. Find the section you want — each one is marked, e.g. `<section id="updates">`.
3. Edit the text, save, then push:
   ```
   git add -A
   git commit -m "update site"
   git push
   ```
4. It is live in 1–2 minutes.

You can also edit `index.html` directly on github.com (pencil icon) from a phone.

## Common edits

**Add an update** — inside `<section id="updates">`, add a `<dt>`/`<dd>` pair at the top:
```html
<dt>Sep 2026</dt>
<dd>Presented preliminary results on bearing fault classification at ...</dd>
```
Do this every 4–8 weeks and keep about eight entries. This is the part of the page that makes people come back and email you.

**Add a paper** — inside `<section id="publications">`, delete the "no papers yet" paragraph and uncomment the `<ol class="refs">` template below it. Bold your own name with `<span class="self">`.

**Add the CV** — put `cv.pdf` in this folder and uncomment the CV line near the top of `index.html`.

**Update the date** — change "Last updated: August 2026" in the footer whenever you make a real change.

There are HTML comments (`<!-- ... -->`) throughout the file with more instructions. They are invisible to visitors.

## Checks worth running after a big change

- Open the page and press Ctrl+P — it should print cleanly as a CV-like document.
- Paste the URL into https://www.linkedin.com/post-inspector/ to refresh the link preview card.
- Paste the URL into https://search.google.com/test/rich-results to confirm the structured data still parses.
