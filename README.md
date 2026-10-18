# A'Jys Enterprise website

Single-page site for A'Jys Enterprise, a direct Interplast dealer on Spintex Road, Accra.
Static HTML, no build step, no dependencies beyond Google Fonts.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site: markup, styles, animations, SEO head, JSON-LD structured data |
| `robots.txt` | Allows search engines and AI crawlers; points to the sitemap |
| `sitemap.xml` | Sitemap for Google Search Console / Bing Webmaster |
| `llms.txt` | Plain-text business summary for AI assistants (Agent Engine Optimization) |

## Deploy

Upload the four files to the root of any static host (Vercel, Netlify, Cloudflare Pages, cPanel `public_html`).
No server-side code is needed.

## Before going live, replace these placeholders

1. **Domain.** `https://ajysenterprise.com/` appears in `index.html` (canonical, Open Graph, JSON-LD), `sitemap.xml`, `robots.txt` and `llms.txt`. Find-and-replace with the real domain.
2. **Social image.** Add `og-image.jpg` (1200 x 630 px, a photo of the shop or stacked Interplast pipes) at the site root. It is referenced by the Open Graph tags and the LocalBusiness schema.
3. **Opening hours.** The page, the schema and `llms.txt` say Monday to Saturday, 8:00 am to 5:00 pm. This is an assumption. Confirm with the owner and edit all three.
4. **Payment methods.** The schema lists "Cash, Mobile Money, Bank transfer". Confirm.
5. **Map pin.** The geo coordinates (5.6365, -0.1175) are an approximate point on Spintex Road. Replace with the exact pin from Google Maps, and update the "Open in Google Maps" link in the contact section with the Google Business Profile link once it exists.
6. **Email.** No email address is shown because none was provided. Add one to the contact section and the JSON-LD `contactPoint` if wanted.
7. **Photos.** Product cards use line illustrations. Real photos of stock, the shop front and completed installs will lift conversion and image search traffic.

## How the quote form works

There is no backend. The form builds a WhatsApp message from the fields and opens `wa.me/233546256657` with the text prefilled. The visitor sends it from their own phone. A copy button covers devices where WhatsApp does not open.

## SEO and AEO checklist after launch

- Create a **Google Business Profile** for "A'Jys Enterprise" at the Spintex Road address with the same phone number. This is the single biggest local-search lever.
- Verify the domain in **Google Search Console** and submit `sitemap.xml`.
- Test structured data at https://validator.schema.org and https://search.google.com/test/rich-results (LocalBusiness and FAQPage should both pass).
- Keep the name, address and phone identical everywhere (site, Google, Facebook, directories).
- Add the site link to any Facebook, Instagram or Jiji listings, and add those URLs to the `sameAs` array in the JSON-LD.
