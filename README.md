# VistaGato — Shopify Storefront Development & Customization

**Professional Client Project | My Amazon Guy (MAG)**

**Role:** Shopify Developer — Theme Customization, Responsive Development & Troubleshooting  
**Platform:** Shopify  
**Technologies:** Shopify Liquid · HTML · CSS · JavaScript · Shopify Theme Editor · Swiper.js · JSON-LD  
**Live website:** [vistagato.com](https://vistagato.com/)

---

## Project Overview

VistaGato is a Shopify eCommerce storefront offering window-mounted cat enclosures, with four featured product lines: **Freedom**, **Signature**, **Premier**, and **Luxe**.

During my work at **My Amazon Guy (MAG)**, I worked on the VistaGato storefront's custom Shopify sections, product presentation, responsive behavior, video interfaces, shopping controls, and related frontend fixes. The project involved adapting an existing Shopify theme and developing purpose-built Liquid sections rather than creating the entire original theme from scratch.

This repository documents **real professional development work**, using screenshots and selected code from the Shopify theme. The code reflects actual implementation details but should be reviewed for client and theme redistribution permissions before publication.

## Development Highlights

- **Custom sections:** Configurable content blocks, responsive images, video presentation, navigation boxes, and product carousels.
- **Product experience:** Gallery video thumbnail indicators, featured-product layout enhancements, product information ordering, and purchase interfaces.
- **Responsive UI:** Distinct desktop and mobile image assets, typography, spacing, layout behavior, and sticky purchase controls.
- **Frontend troubleshooting:** Product gallery positioning, responsive presentation, review-related anchor behavior, and visibility of checkout options.
- **Search optimization implementation:** VideoObject JSON-LD output for configured product and section videos. Schema validity and indexing are not claimed without separate validation.

---

## Storefront Screenshots

Screenshots illustrate the storefront experience and the components associated with the development work. Their presence does not mean every part of each page was independently built by me.

### Homepage — Hero

![VistaGato homepage hero](<01 - Homepage/VistaGato_01_Homepage.png>)

The main homepage banner introduces the VistaGato brand and product offering.

### Homepage — Our Vistas

![VistaGato Our Vistas homepage section](<01 - Homepage/VistaGato_02_Our_Vistas.png>)

The "Our Vistas" section presents the four product models in a comparison-oriented layout.

### Product Detail Pages

**VistaGato Signature**

![VistaGato Signature product detail page](<02 - Product Detail Pages/VistaGato_03_Signature_Product_Page.png>)

**VistaGato Premier**

![VistaGato Premier product detail page](<02 - Product Detail Pages/VistaGato_04_Premier_Product_Page.png>)

**VistaGato Luxe**

![VistaGato Luxe product detail page](<02 - Product Detail Pages/VistaGato_05_Luxe_Product_Page.png>)

**VistaGato Freedom**

![VistaGato Freedom product detail page](<02 - Product Detail Pages/VistaGato_06_Freedom_Product_Page.png>)

The product-page screenshots show gallery thumbnails, product descriptions, displayed prices, reviews, and available or sold-out purchasing states at the time of capture. Store prices and inventory can change.

---

## Technical Spotlight 1 — Featured Product Layout & Mobile Sticky Cart

**Source:** [`new-featured-product.liquid`](<03 - Custom Code/new-featured-product.liquid>)

This customized Shopify featured-product section contains substantial Liquid, CSS, and JavaScript work, including:

- Mobile reordering of title, review stars, image gallery, price, and content blocks.
- Desktop sticky gallery positioning and layout adjustments.
- Responsive section-spacing controls in the Shopify Theme Editor.
- Custom video thumbnail play-button styling.
- Styling for side-by-side express payment options.
- A fixed mobile purchase bar with product image, title, price, quantity controls, and a Shopify product form.
- Selected-variant synchronization between the product controls and mobile purchase bar.
- Sold-out purchase states based on Shopify availability.
- VideoObject JSON-LD generation for configured product media.
- A targeted workaround for review-text/anchor behavior.

**Implementation note:** Some fixes use forceful CSS overrides and a recurring DOM-style check. They document real troubleshooting work in an existing theme, rather than a generalized, production-ready library.

## Technical Spotlight 2 — Custom Landing Page, Anchor Boxes & Video Content

**Source:** [`magcustom2.liquid`](<03 - Custom Code/magcustom2.liquid>)

This configurable section combines:

- Two navigation boxes with **separate desktop and mobile anchor destinations**.
- Theme Editor settings for headings, copy, background, spacing, text alignment, and desktop/mobile images.
- Support for **two Shopify-hosted videos** in a responsive layout.
- Animated custom play buttons and JavaScript click-to-play interactions.
- Configurable VideoObject metadata, output as JSON-LD.

The code contains the structured-data implementation; successful search-engine eligibility has not been independently verified.

## Technical Spotlight 3 — Custom Product Carousel

**Source:** [`magcustom9.liquid`](<03 - Custom Code/magcustom9.liquid>)

This collection-driven section includes:

- Responsive Swiper.js product carousel with breakpoint-based slide counts.
- Product cards with images, titles, prices, optional compare-at prices, and variant counts.
- Add-to-cart forms or disabled sold-out buttons, based on product availability.
- Configurable promotional badges, arrows, pagination dots, colors, typography, and spacing.
- An optional section anchor for linking to the displayed collection.

**Implementation note:** Its supplied initialization targets the first matching `.magcustom9 .product-carousel`. Multiple carousels on the same page would require an additional review.

## Technical Spotlight 4 — Product Video Thumbnail UI

**Source:** [`product-media.liquid`](<03 - Custom Code/product-media.liquid>)

The theme's product-media snippet includes custom styling and markup for video thumbnails:

- Centered circular play icons on gallery thumbnails.
- Hover and pulsing animations.
- Video and external-video detection in multiple media layouts.

This file also contains underlying existing Shopify/theme gallery markup. The separate minified `product-media.js` gallery engine has **not** been included as independently authored code.

## Technical Spotlight 5 — Additional Custom Content Sections

| File | Purpose |
|---|---|
| [`magcustom4.liquid`](<03 - Custom Code/magcustom4.liquid>) | Responsive full-width image with an optional link and new-tab setting |
| [`magcustom5.liquid`](<03 - Custom Code/magcustom5.liquid>) | Configurable founder/profile-style content with thumbnail-to-video playback |
| [`magcustom6.liquid`](<03 - Custom Code/magcustom6.liquid>) | Independently scoped variation of the configurable video/profile section |
| [`magcustom7.liquid`](<03 - Custom Code/magcustom7.liquid>) | Content section with different desktop/mobile images and responsive typography |

The `magcustom5` and `magcustom6` sections are similar in structure, with separate CSS classes, setting identifiers, and default styling.

---

## Technology Stack

| Technology | Role in this project |
|---|---|
| Shopify | Storefront, products, collections, and checkout integration |
| Shopify Liquid | Dynamic section markup, product details, media, forms, and configurable settings |
| HTML/CSS | Responsive layout, galleries, video buttons, cards, and sticky purchase components |
| JavaScript | Video interactions, gallery-related adjustments, purchase controls, and carousel behavior |
| Shopify Theme Editor | Merchant-configurable section content, layout, and styling |
| Swiper.js | Responsive product-card carousel in `magcustom9.liquid` |
| JSON-LD / Schema.org | VideoObject structured-data markup for configured videos |

## Repository Structure

```text
vistagato-shopify/
├── 01 - Homepage/
│   ├── VistaGato_01_Hero.png
│   └── VistaGato_02_Our_Vistas.png
├── 02 - Product Detail Pages/
│   ├── VistaGato_03_Signature_Product_Page.png
│   ├── VistaGato_04_Premier_Product_Page.png
│   ├── VistaGato_05_Luxe_Product_Page.png
│   └── VistaGato_06_Freedom_Product_Page.png
├── 03 - Custom Code/
│   ├── product-media.liquid
│   ├── new-featured-product.liquid
│   ├── magcustom2.liquid
│   ├── magcustom4.liquid
│   ├── magcustom5.liquid
│   ├── magcustom6.liquid
│   ├── magcustom7.liquid
│   └── magcustom9.liquid
└── README.md
```

**File-path note:** This layout assumes the screenshots and code are uploaded using the exact filenames shown. Update links if your local filenames differ. The files are selected theme code snapshots, **not** a complete Shopify theme export.

---

## What This Project Demonstrates

- Hands-on Shopify Liquid development and section customization.
- Responsive storefront implementation and UI debugging.
- Product presentation and video-thumbnail interface customization.
- Swiper product carousel and collection merchandising integration.
- Shopify product-form, purchase-state, and mobile sticky-cart interfaces.
- SEO-related structured data implementation for videos.
- Ability to work within and troubleshoot an existing commercial theme.

## Attribution & Sharing

This work was carried out as part of my Shopify Developer role at **My Amazon Guy (MAG)** for **VistaGato**. The portfolio describes development and fixes I worked on; it does not claim authorship of the original commercial Shopify theme, all storefront content, or third-party components.

Client branding, imagery, existing theme components, and third-party libraries retain their respective ownership. **Editing access is not necessarily permission to republish full commercial theme files.** Before uploading source code to a public repository, confirm portfolio-sharing permission and exclude confidential content, secrets, and third-party source not authorized for redistribution. If permission is limited, publish the README/screenshots and a sanitized, independently authored demonstration of the relevant custom logic instead.

---

**Portfolio maintained by Rocky Romorosa**  
Shopify & eCommerce Developer
