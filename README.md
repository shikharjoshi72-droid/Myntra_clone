# Myntra Exclusive Performance Techwear: Storefront

A responsive, single-page e-commerce storefront for a performance techwear collection. It is built with plain HTML, CSS and vanilla JavaScript, so it needs no build step, framework or backend.

## Features

- **Product catalog:** 12 products with price, discount, rating, sizes, colors and fabric tech.
- **Navigation tabs:** ALL, MEN, WOMEN, NEW ARRIVALS and SALE (35% off or more).
- **Search:** live search by product name, category or fabric tech.
- **Filters:** category, price slider and presets, size, color and fabric tech. Several filters can be combined.
- **Active filter pills:** remove a single filter or clear them all.
- **Sorting:** recommended, price (low to high or high to low), customer rating and new arrivals.
- **Grid layout toggle:** switch between 3 and 4 columns.
- **Quick view modal:** product details, fabric tech description and size selection.
- **Wishlist drawer:** save items, remove them, or move them to the bag.
- **Shopping bag drawer:** quantity controls and a live total (MRP, discount and final amount).
- **Mobile filter drawer** and **toast notifications**.

## Project Structure

```
.
├── index.html   # Page structure and markup
├── style.css    # Styling (linked from index.html)
├── script.js    # Product data, state, rendering and event logic
└── README.md
```

## Getting Started

1. Put `index.html`, `style.css` and `script.js` in the same folder.
2. Open `index.html` in any modern browser.

Optionally, serve it locally:

```bash
# Python
python -m http.server 8000

# or Node
npx serve .
```

Then visit `http://localhost:8000`.

## How It Works

`script.js` is organized into these sections:

| Section | Purpose |
|---|---|
| `PRODUCTS` | Array of product objects (catalog data) |
| `state` | Single object holding filters, sort order, wishlist and cart |
| DOM references | Cached element lookups |
| `getFilteredProducts()` | Applies tab, search, filters and sorting |
| `renderProducts()` | Builds product cards and attaches handlers |
| Wishlist and cart functions | Add, remove, move and total calculations |
| Quick view functions | Open and close the product modal |
| `initEvents()` | Registers all event listeners |

The page re-renders from `state` whenever a filter, tab, sort option or search term changes.

## Customization

**Add a product:** append an object to the `PRODUCTS` array in `script.js`:

```js
{
  id: 13,
  title: 'YOUR PRODUCT',
  brand: 'MYNTRA LABS',
  category: 'Shoes',            // T-Shirts | Jackets | Shoes
  price: 4999,
  originalPrice: 8999,
  discount: '44% OFF',
  rating: 4.8,
  reviewsCount: 100,
  fabricTech: 'Aero-Weave',     // Aero-Weave | Thermo-Regulating | Thermo-Peep | Aero-Shirrt
  techDescription: 'Short description.',
  colors: ['Grey', 'Teal'],
  sizes: ['S', 'M', 'XL'],
  image: 'https://...',
  tag: 'LABEL',
  gender: 'Men',                // Men | Women
  isNew: true
}
```

**Change the max price:** update `54900` in `state`, the slider's `max` and `value` in `index.html`, and the reset logic in `script.js`.

## Notes and Known Limitations

- The wishlist and bag are kept in memory only and reset on page reload.
- Checkout is a demo. It shows a confirmation toast and empties the bag.
- Some functions (`resetAllFilters`, `removeSingleFilter`, `toggleWishlist`, `addToCart` and others) must stay global because the generated HTML calls them through inline `onclick` attributes.
- The mobile filter drawer copies the sidebar HTML without re-attaching event listeners, so its controls do not work yet.
- Product images are loaded from Unsplash and need an internet connection.

## Tech Stack

HTML5, CSS3, vanilla JavaScript (ES6+), and Google Fonts (Inter and Outfit).

## License

For demonstration and learning purposes. Add your preferred license here.

//===================================================================================================================================================//

# Myntra_clone

### Check out my Myntra_clone!

[![LIVE WEBSITE](https://img.shields.io/badge/LIVE-WEBSITE-brightgreen?style=for-the-badge&logo=vercel)](https://myntraclone-chi.vercel.app/)
