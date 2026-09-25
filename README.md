# Elitsa Lash & Brow — portfolio website

A one-page website for a lash lift and brow lamination business, written in plain HTML and CSS. There's no JavaScript, no build step and nothing to install.

Sections: **Services & pricing** (with FAQ/aftercare), **My work** (before & after, lashes, brows), **Client reviews**, **About** and **Contact / booking**.

## Files

```
public/index.html          ← all the text, services, photos and reviews
public/css/styles.css      ← the look (colours are at the top of the file)
public/images/             ← hero and about photos, favicon
public/images/gallery/     ← your work photos
wrangler.jsonc             ← Cloudflare settings (no need to touch)
```

## Preview it

Double-click `public/index.html` to open it in your browser.

## Editing

Everything is in `public/index.html`. Each section starts with a comment like `<!-- ===== SERVICES ===== -->` that explains what to change.

### Add a photo of your work
1. Put the photo in `public/images/gallery/`, e.g. `public/images/gallery/brows-june.jpg`. Square photos under about 500 KB work best.
2. In `public/index.html`, find the **Lashes** or **Brows** gallery, copy one block and change the file name and caption:
   ```html
   <figure class="work">
     <a href="images/gallery/brows-june.jpg"><img src="images/gallery/brows-june.jpg" alt="Laminated brows" loading="lazy"></a>
     <figcaption>Brow lamination & tint</figcaption>
   </figure>
   ```
3. For a before & after, copy a `<figure class="work work--pair">` block from the **Before & after** gallery and set both images.

### Add a review
Copy one `<figure class="review">` block, paste it at the top of the list and change the name, stars (`★★★★★`), treatment, date and text. Only post real reviews, and ask your clients before you do.

### Change services and prices
Edit the `<article class="service">` blocks. To add a "Most popular" label to a service, give it `class="service service--featured"`.

### Other things to replace
- The phone number, email, address and opening hours in the **Contact** section
- The **Book now** button link. Point it at your booking page (Fresha, Booksy, Calendly, WhatsApp…) or leave it as your email.
- The Instagram link in the footer
- The "Leave a review" link in the reviews section (your Google review link)
- `public/images/hero.svg` and `public/images/about.svg`: add your own photos (e.g. `hero.jpg`) and update the `src` in `public/index.html`
- The placeholder photos in `public/images/gallery/`

### Change colours
Open `public/css/styles.css` and edit the values at the top (`--accent`, `--bg` and so on).

## Publish it for free with Cloudflare
1. In the Cloudflare dashboard go to **Workers & Pages → Create application**.
2. Choose **Import a repository** (Continue with GitHub) and pick this repository.
3. Leave the **build command** empty. The **deploy command** should be `npx wrangler deploy` (the default).
4. Click **Deploy**. The site goes live at `https://elitsa-dankov.<your-subdomain>.workers.dev`.

Every time a change is pushed to GitHub, Cloudflare publishes it automatically. You can add your own domain later under the project's **Settings → Domains & Routes**.
