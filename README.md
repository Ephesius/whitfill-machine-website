# Whitfill Machine & Welding website

Plain HTML and CSS. No build step, no framework, no database. Any host that serves
files will run it.

```
index.html          Home
services.html       Services
gallery.html        Gallery
quote.html          Request a quote (form)
employment.html     Employment application (form, plus a printable version)
contact.html        Contact
404.html            Shown when someone mistypes an address
assets/css/style.css    All styling. Colors are at the top under :root.
assets/img/             Logo variants, link preview image, photo placeholders.
```

## To preview it

Double-click `index.html`. The map stays blank until the site is on a real web
server. Everything else works.

## Things that still need you

All the text is written. Rewrite any of it in your own words whenever you like.

Two facts are worth checking before the site goes public: the shop hours on
`contact.html` say Monday through Friday, and nothing on the site names a founding
year or an owner. Add a sentence about either to the about section on `index.html`
if you want it there.

**Captions.** The gallery has no captions. To add one, put a `<figcaption>` line
inside a figure, like this:

```html
<figure>
  <img src="assets/img/shop-01.jpg" alt="A vertical mill cutting a steel plate">
  <figcaption>Roughing a mounting plate</figcaption>
</figure>
```

**Photos.** Every grey dashed box marked "Photo" is a placeholder. Replace the file
in `assets/img/` with a real photo of the same name, or point the `<img src="...">`
at your new filename. Aim for roughly 1600px wide, saved as JPG, under about 400 KB.

**Alt text.** Each placeholder has an empty `alt=""`. When you swap in a real photo,
write a plain description of the picture there. That text is what a blind visitor
hears and what search engines read.

**Service photos are optional.** If you have no picture for one of the seven
services, delete that service's `<img>` tag and the text widens to fill the space.
Nothing breaks, so you can add photos a few at a time.

## Forms

Both forms are built but have nowhere to send data yet. Once you pick a host, sign
up for a form service and paste its address into the `action="#"` attribute on
`quote.html` and `employment.html`.

- **Netlify Forms**: free if the site is hosted on Netlify. Add `netlify` to the
  `<form>` tag and you are done. Submissions arrive by email and in a dashboard.
- **Formspree**: works on any host, free tier suits a small shop.

**File uploads.** Both forms accept attachments, but whether they go through depends
on the form service. Test it before relying on it. The quote page also invites people
to email drawings directly, which is a safe fallback.

## Printable employment application

The "Print a blank application" button opens the print dialog with a stylesheet that
strips the navigation and turns the fields into ruled lines. From there anyone can
print it or choose "Save as PDF", so you get a paper application without keeping a
separate PDF up to date.

## Link previews

When the site address is shared in a text message or on social media, a preview card
appears. `assets/img/og-image.png` is that image, currently the logo on navy. Once
you have a good photo of the shop, replace that file with a 1200 by 630 pixel version
of it for a stronger preview.

The preview tags in each page point at `https://whitfillmachine.com`. If the site
ends up at a different address, search the files for `whitfillmachine.com` and update
those lines.

## The logo

The original SVG is drawn in white, which is why it looks blank on a white
background. Four versions are in `assets/img/`:

- `logo-navy.svg` and `logo-white.svg`: full logo with the wordmark
- `mark-navy.svg` and `mark-white.svg`: just the welder emblem, no text

The header uses the white emblem beside type. The footer uses the full white logo.
To change the color, open the file in a text editor and change the one `fill` value.

## Colors

Set in `assets/css/style.css`:

| Token | Value | Used for |
|---|---|---|
| `--navy` | `#10314e` | Header, headings, buttons |
| `--navy-deep` | `#0a2035` | Footer |
| `--navy-tint` | `#eef2f6` | Alternating section background |
| `--spark` | `#c8901f` | Accent: quote button, rule beside the hero |

Changing a value there changes it everywhere.
