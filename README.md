# Redline Dumpsters — Website

A static one-page website for a roll-off dumpster rental business, styled in a
red/black industrial theme. Built with plain HTML/CSS/JS — no build step, no
dependencies to install. Ready to publish on GitHub Pages.

## What's inside

```
index.html        The whole page (sections: hero, sizes, process, services,
                   accepted items, service area, testimonials, FAQ, contact)
css/style.css      All styling and design tokens (colors, fonts, layout)
js/script.js       Mobile nav toggle, FAQ accordion, quote form handling
```

## Placeholder content — update before you launch

Everything below is a placeholder. Use your editor's find-and-replace across
`index.html` (and the footer) to swap these in:

| Placeholder | Find | Replace with |
|---|---|---|
| Business name | `Rose Roll-Offs LLC` | Your real business name |
| Phone number | `(816) 582-2269` and `tel:+18165822269` | Your real number |
| Email | `roserolloffs@gmail.com.com` | Your real email |
| Address | `Weston, MO and surrounding` | Your real address |
| Pricing | `$370` | Your real rates |
| Service area cities | the `<ul class="area-list">` list | Cities you actually serve |
| Testimonials | the "Sample Customer" cards | Real reviews once you have them |

The hero illustration and all icons are original SVG (no stock photos), so
there's nothing to license — but you're welcome to swap in real photos of your
trucks/bins. Just drop images into the `images/` folder and reference them
with `<img src="images/yourfile.jpg">`.

## Making the quote form actually work

Right now the "Request a Free Quote" form only shows a placeholder success
message — it doesn't send anywhere. GitHub Pages only serves static files, so
you need a small external service to receive submissions. Easiest options:

- **Formspree** (formspree.io) — add `action="https://formspree.io/f/YOUR_ID"`
  and `method="POST"` to the `<form>` tag in `index.html`, remove the
  JavaScript `preventDefault()` handling in `js/script.js`, and it just works.
- **Netlify Forms** — if you host on Netlify instead of GitHub Pages, add
  `data-netlify="true"` to the `<form>` tag and it's handled automatically.

## Publishing to GitHub Pages

1. Create a new repository on GitHub (e.g. `redline-dumpsters`).
2. Upload these files to the repo, keeping the folder structure intact
   (`index.html` at the root, `css/` and `js/` folders alongside it).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   choose branch `main` and folder `/ (root)`, then click **Save**.
5. GitHub will give you a URL like `https://yourusername.github.io/redline-dumpsters/`
   — it can take a minute or two to go live.
6. (Optional) If you have a custom domain, add it under Settings → Pages →
   Custom domain, and set up the DNS records GitHub shows you.

If you'd rather do this from the command line:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/redline-dumpsters.git
git push -u origin main
```

Then follow steps 3–5 above to turn on Pages.

## Customizing the look

All colors, fonts, and spacing live at the top of `css/style.css` in the
`:root` block — change a value there and it updates everywhere. For example,
to shift the red to a different shade, just change `--red` and `--red-bright`.

## Browser support

Plain HTML/CSS/JS, no build tools, works in all modern browsers. Mobile nav
collapses under ~720px width; layout is responsive down to phone widths.
