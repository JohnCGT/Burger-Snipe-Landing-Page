# Burger Snipe 🍔

A multi-page landing site for a fictional burger restaurant, **Burger Snipe**. Built with plain HTML, CSS, and vanilla JavaScript, with Bootstrap 5 for layout/navigation and Tailwind CSS for the ordering interface.

## Pages

| Page | File | Description |
|---|---|---|
| Home | `index.html` | Hero banner, tagline, and a filterable preview of the menu (All / Best Seller / Classic / Deluxe categories). |
| Menu | `menu.html` | Full menu grid with the same category filtering. |
| About | `about.html` | Information about the restaurant. |
| Order | `order.html` | Interactive ordering screen — browse items, search, add quantities to a running order, see a live total, and "pay" against an entered amount to get change. |

## Features

- Responsive Bootstrap navbar shared across all pages
- Category filter buttons (`All`, `Best Seller`, `Classic Burger`, `Deluxe Burger`) that show/hide menu items via JavaScript `data-category` attributes
- Live-search on the order page that filters items as you type
- Client-side "cart" that tracks quantities and computes a running total (in PHP)
- Simple checkout flow that validates payment amount and calculates change
- Google Fonts (`Dancing Script`, `Poppins`) for branding/typography

## Tech Stack

- HTML5 / CSS3
- Vanilla JavaScript (no build step or framework)
- [Bootstrap 5.3.3](https://getbootstrap.com/) (via CDN) — navigation and layout on Home/Menu/About
- [Tailwind CSS](https://tailwindcss.com/) (via CDN) — styling on the Order page
- Google Fonts (via CDN)

## Project Structure

```
Burger-Snipe-Landing-Page-main/
├── index.html          # Home page
├── menu.html            # Menu page
├── about.html            # About page
├── order.html            # Ordering page (menu + cart logic)
├── css/
│   └── styles.css       # Shared styles for Home/Menu/About
└── resources/            # Burger images used across the site
```

> **Note:** `order.html` links to `css/order.css`, which is not included in this repo. Add that file (or remove the link) if you need page-specific styling for the order screen beyond the Tailwind utility classes already used inline.

## Getting Started

No build tools or dependencies to install — this is a static site.

1. Clone or download this repository.
2. Open `index.html` in your browser (or serve the folder with any static file server, e.g. `npx serve` or the VS Code "Live Server" extension).
3. Navigate the site using the top nav bar: **Home → Menu → About → Buy Now (Order)**.

## Menu Items

The order page currently includes:

- Cheese Burger — ₱259
- Truffle Burger — ₱289
- Black Bean Burger — ₱279
- Bacon Burger — ₱239
- Wagyu Beef Burger — ₱269
- Mushroom Melt Burger — ₱219
- Double Patty Burger — ₱309
- Brie Bliss Burger — ₱329
- Lentil Patty Burger — ₱229

Items and prices are defined as a plain JavaScript array (`items`) directly in `order.html`, so they're easy to edit without touching any other files.
