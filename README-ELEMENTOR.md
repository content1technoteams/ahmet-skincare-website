# AHMET CİLT BAKIMI LTD. · Responsive Website Package

## Pages included

- `index.html` — Home
- `brands.html` — Our Brands
- `products.html` — Product collection and interactive filters
- `turhan.html` — TURHAN Skin Lightening Cream
- `lumi-clear.html` — **New** LUMI CLEAR™ Acne & Blemish Care Cream
- `about.html` — About Us
- `wholesale.html` — Wholesale & Distribution
- `contact.html` — Contact and interactive inquiry form

The shared styling is `assets/css/style.css`; interaction code is `assets/js/site.js`; images (including crops from supplied UI/UX designs and original supplied brand graphics) are in `assets/img/`.

## Preview

Open `index.html` in a browser, or serve the folder with `python -m http.server 8000` and visit `http://localhost:8000/`. All relative links work from the same folder. The source is plain HTML, CSS, and JavaScript: no build pipeline, tracking scripts, external libraries or paid fonts.

## WordPress + Elementor workflow

**This package is Elementor-friendly but is not an installable WordPress theme or an Elementor JSON template.** For a maintainable WordPress implementation:

1. Install a lightweight theme such as Hello Elementor and create eight WordPress pages with matching slugs: `/`, `/our-brands/`, `/products/`, `/turhan/`, `/lumi-clear/`, `/about/`, `/wholesale/`, `/contact/`.
2. Recreate the layouts with **Elementor Containers** following the HTML sections. Set global typography to Georgia (headings) and system sans-serif (body), primary color `#aa8350`, ink `#25323b`, ivory `#faf8f4`, and section width approximately 1180px.
3. Upload the images from `assets/img` to the WordPress Media Library and substitute Media Library URLs for local `assets/img/...` paths. Some brand images are sourced as crop excerpts from supplied design mockups; replace with original studio assets when available for print-quality use.
4. Set the global Header/Footer in Elementor Theme Builder. Use the included HTML for copy, hierarchy and link mapping. **Replace relative `.html` links with WordPress permalinks.**
5. For dynamic editing, build an Elementor Loop/Grid using a Products custom post type (CPT UI, ACF or native custom fields) with brand, headline, introduction, weight, origin, product gallery, FAQs, product benefits, and disclosure fields. Use Elementor dynamic tags instead of hard-coded HTML cards.
6. For the accordion use Elementor Accordion; for tabs use Nested Tabs; for the filterable product catalogue use Elementor Loop Grid plus a taxonomy filter. For image galleries use Elementor galleries. For animation use modest Entrance Animations and CSS transitions, respecting `prefers-reduced-motion`.
7. Replace the demo **mailto** form with **Elementor Forms, WPForms or Gravity Forms**. Configure delivery addresses, antispam, privacy notice, consent, and server-side validation. The static demo form *does not submit to a server*, and instead prepares an email in the visitor's default email application.
8. Add `assets/css/style.css` to a child theme or Elementor Site Settings > Custom CSS (Elementor Pro). Add `assets/js/site.js` via a child theme enqueue or a permitted Custom Code integration; do not add duplicate scripts when using native Elementor widgets.
9. Confirm accessibility, mobile breakpoints, focus states, image alt text, performance and all links on the actual WP installation.

## Important launch checks

- Confirm TURHAN final **20g** packaging. The website design screenshot depicts a different tube size and illustrative product variants. The current product reference uses the supplied actual TURHAN cream imagery.
- Confirm LUMI CLEAR final ingredients, usage directions and claims with the manufacturer. The proposed ingredient list is explicitly labelled as unconfirmed.
- TURHAN GMP / ISO / HALAL, LUMI CLEAR awards, clinical/dermatological certifications and before/after claims in supplied artwork are **not independent proof**. This site does not assert those claims as verified.
- NOORÉA and ancillary TURHAN product photos are shown in the mockup references and may be illustrative concepts, not verified stocked products. Confirm current availability before publishing.
- The contact emails `info@skincareahmet.com` and `wholesale@skincareahmet.com` were shown as placeholders in the designs. Confirm actual operational inboxes.
- Social links currently point to the platforms' homepages. **Replace with your official profile URLs** before launch.
- Review company name spelling, legal details, privacy policy, cookie policy and current year with counsel/developer. The footer credits **Designed & Developed by TechoTeams**, as requested.
- Product reviews: do not publish invented reviews as genuine Verified Purchase feedback. Source real, consented reviews through WordPress.

## Features

Responsive sticky navigation, mobile menu, smooth anchored scrolling, intersection-based reveal animations, interactive product filters, gallery thumbnails with zoom modal, accessible FAQ accordions, product information tabs, form validation and mailto handoff, semantic landmarks, reduced-motion support and shared footer on every page.

## Layout correction update — 21 November 2026
This revision corrects the product-card image anchors to block/flex layout, gives every product image a controlled aspect ratio, prevents card and footer collision, and improves responsive behavior for desktop, tablet and mobile. The two confirmed product photo sets use their higher-resolution campaign assets. Small concept-product cutouts sourced from the UI mockups have been moderately sharpened and are displayed in contained frames; they do not contain genuine new source detail. For print-level sharpness, replace concept imagery with original high-resolution product photography.

In Elementor, set product listing containers to a Grid or Flexbox, give each image a fixed **aspect ratio**, choose **Object Fit: Contain**, set cards to **height: 100%** and keep footer as a separate, full-width section below `<main>`. Do not paste the site-wide stylesheet into each Elementor widget, as duplicate style rules could conflict with the theme.
