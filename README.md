# Elitsa Lash & Brow — portfolio website

A one-page website for a lash lift and brow lamination business, written in plain HTML and CSS. There's no JavaScript, no build step and nothing to install.

Sections: **Services & pricing** (with FAQ/aftercare), **My work** (before & after, lashes, brows), **Client reviews**, **About** and **Contact / booking**.

## Files

```
index.html            ← all the text, services, photos and reviews
css/styles.css        ← the look (colours are at the top of the file)
images/               ← hero and about photos, favicon
images/gallery/       ← your work photos
```

## Preview it

Double-click `index.html` to open it in your browser.

## Editing

Everything is in `index.html`. Each section starts with a comment like `<!-- ===== SERVICES ===== -->` that explains what to change.

### Add a photo of your work
1. Put the photo in `images/gallery/`, e.g. `images/gallery/brows-june.jpg`. Square photos under about 500 KB work best.
2. In `index.html`, find the **Lashes** or **Brows** gallery, copy one block and change the file name and caption:
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
- `images/hero.svg` and `images/about.svg`: add your own photos (e.g. `hero.jpg`) and update the `src` in `index.html`
- The placeholder photos in `images/gallery/`

### Change colours
Open `css/styles.css` and edit the values at the top (`--accent`, `--bg` and so on).

## Publish it for free with GitHub Pages
1. On GitHub, open the repository and go to **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, pick your branch (e.g. `main`) and the `/ (root)` folder, then click **Save**.
3. After a minute or two the site will be live at `https://<your-username>.github.io/<repo-name>/`.

You can connect your own domain later from the same page.
