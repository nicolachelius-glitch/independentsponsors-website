# [Firm Name] — Website

A five-page static brochure site for an independent sponsor. Plain HTML and CSS —
no build step, no framework, no dependencies to maintain. Drop it into a GitHub
repo, switch on GitHub Pages, point the domain, and it's live.

## Files

```
index.html        Home — hero, philosophy intro, approach preview
about.html        Principal bios + firm story
approach.html     Investment philosophy, criteria, process
investments.html  Track record / selected investments
contact.html      Listed emails (no form — nothing to break)
styles.css        All styling (edit colours/fonts here)
main.js           Mobile menu toggle only
```

## How to fill it in

Every editable spot is marked with `[square brackets]`. Search each file for `[`
and replace with real content. The big ones:

- **`[Firm Name]` / `[Firm]`** — appears in the nav brand, titles, and footer of
  every page. Do a find-and-replace across all files.
- **`independent-sponsors.co.za`** and the `[name1]` / `[name2]` email addresses on
  `contact.html` — set these to their real addresses.
- **Bios** on `about.html`, **criteria** on `approach.html`, **deals** on
  `investments.html`.

### Adding a photo for a principal
On `about.html`, find the `<div class="portrait">Photo</div>` and change it to:
```html
<div class="portrait" style="background-image:url('images/principal-1.jpg')"></div>
```
Put the image in an `images/` folder next to the HTML. Portrait orientation
(roughly 4:5) works best.

### Adding or removing an investment
On `investments.html`, copy or delete a whole `<article class="deal">…</article>`
block. The list grows or shrinks automatically.

### Changing colours or fonts
Open `styles.css` — every colour is defined once at the top under `:root`.
Change a hex value there and it updates everywhere.

## Putting it live on GitHub Pages (free, custom domain)

1. Create a new repository on GitHub (e.g. `firm-website`).
2. Upload all these files to the repository root (drag-and-drop in the GitHub
   web UI works fine — no command line needed).
3. Go to **Settings → Pages**. Under "Build and deployment", set Source to
   **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. After a minute the site is live at `https://<username>.github.io/<repo>/`.
5. To use the firm's own domain, in the same Pages settings enter the custom
   domain (e.g. `www.theirfirm.co.za`) under "Custom domain".
6. Ask the SA email host to add the DNS records GitHub shows you — a `CNAME`
   for `www` pointing at `<username>.github.io` (or the four A records GitHub
   lists for an apex/root domain). **Tell them not to touch the MX records** so
   email keeps working untouched.
7. Tick **Enforce HTTPS** once the certificate provisions (can take an hour).

That's it. To make a change later, edit the file in GitHub (pencil icon) and
commit — the site redeploys on its own.

## Editing locally first (optional)

Just open any `.html` file in a browser to preview. No server needed.
```
```
