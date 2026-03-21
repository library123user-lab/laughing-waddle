# Mwinsi Nkosi Health Care Group — static website

| Page | Purpose |
|------|--------|
| `index.html` | Home — mission, services, contact, **FormSubmit** form |
| `rates.html` | Rates + **billing transparency** (VAT, quotes, travel, cancellation, medical aid placeholders) |
| `legal.html` | **Terms** (placeholder) + **complaints** (placeholder) |
| `thank-you.html` | Optional post-form page (use with `_next` when hosted) |
| `images/` | Drop photos here; wire them in HTML when ready |

Stack: **HTML + CSS** + small **JS** (mobile menu, year).

## Contact form (FormSubmit)

1. The form posts to **`https://formsubmit.co/hello@mwinsinkosi.co.za`**. Change the email in `action="…"` if you use another inbox.
2. **First submission:** check that inbox and **activate** the form (link from FormSubmit).
3. **After you have a live URL:** uncomment/add a hidden field in `index.html`:  
   `name="_next"` and `value="https://YOUR-DOMAIN.com/thank-you.html"`  
   so people return to your site after sending (FormSubmit needs a **full** URL).

## Replace everywhere

- **Phone & WhatsApp** — `+27000000000` and `wa.me/27000000000` (use digits only in `wa.me`, no `+` or spaces).
- **Footer / legal** — company legal name, **CIPC reg**, **VAT**, **physical address**.
- **Complaints email** in `legal.html` — `complaints@…` if different from hello@.
- **Photo** — replace the dashed **image placeholder** on the home page with `<img src="images/yourfile.jpg" alt="…">` or a CSS `background-image` when you have assets.

## View locally

Open `index.html` in the browser, or run `npx serve .` in this folder.

## Figma

The `.fig` file lives in the parent folder; this folder is the live site you can host (Netlify, GitHub Pages, etc.). Use **HTTPS** when live so the form and WhatsApp links behave well.
