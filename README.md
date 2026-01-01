# BookNest
 # Premium Drink Subscription - Shopify Product Page

A modern, responsive product page for a premium drink subscription service built with HTML, Tailwind CSS, and vanilla JavaScript. Features an interactive gallery, flavor selection, and flexible purchase options.

## 📋 Project Overview

This project provides a complete e-commerce product page template for a drink subscription service with:
- **Dynamic product gallery** with image navigation and thumbnails
- **Multiple purchase options** (single or double flavor subscriptions)
- **Interactive flavor selection** with visual color swatches
- **Real-time pricing calculations** with discount tiers
- **Responsive design** optimized for mobile, tablet, and desktop
- **Toast notifications** for user feedback
- **Shopify theme integration** ready for deployment

## 📁 Project Structure

```
figma-workshop/
├── product-page.html           # Standalone HTML product page
├── README.md                   # This file
└── shopify-product-page/       # Shopify theme files
    ├── tailwind.config.js      # Tailwind CSS configuration
    ├── assets/                 # Theme assets (images, fonts, etc.)
    └── sections/
        └── product-custom.liquid # Shopify Liquid template
```

## ✨ Features

### Product Gallery
- Main image display with previous/next navigation
- Thumbnail gallery with active state indicator
- Smooth image transitions
- Click-to-select thumbnail functionality

### Flavor Selection
- Visual color swatches for flavor options
- Active state styling with border and shadow effects
- Dynamic flavor display based on subscription type
- Flavor-1 (required) and Flavor-2 (double subscription only)

### Purchase Options
- **Single Plan**: One flavor monthly with 25% subscription discount
- **Double Plan**: Two flavors monthly (mix and match) with additional 20% off

### Pricing System
- Base price display
- Subscription discount calculation (25% off)
- Additional sales discount (20% off final price)
- Real-time savings calculation
- Price updates based on selection changes

### User Experience
- Toast notification system for user actions
- Form validation before cart addition
- Responsive button states (hover, active)
- Mobile-optimized layout with Tailwind CSS

## 🛠️ Technologies Used

- **HTML5** - Semantic markup
- **Tailwind CSS** - Utility-first CSS framework
- **JavaScript (Vanilla)** - No dependencies required
- **Shopify Liquid** - Theme templating language
- **Responsive Design** - Mobile-first approach

## 🚀 Getting Started

### View the Standalone Page
1. Open `product-page.html` in your web browser
2. Interact with the gallery, select flavors, and test the purchase flow

### Tailwind CSS Setup
The project uses Tailwind CSS from CDN:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

For development with custom build:
```bash
npm install
npx tailwindcss -i ./input.css -o ./output.css --watch
```

### Shopify Integration
1. Copy files from `shopify-product-page/` to your Shopify theme
2. Configure `tailwind.config.js` for your brand colors and styles
3. Customize `product-custom.liquid` with your product data
4. Update product images and pricing in the Liquid template

## 📱 Responsive Breakpoints

- **Mobile**: Default (< 640px)
- **Tablet**: `sm:` (640px+) and `lg:` (1024px+)
- **Desktop**: `lg:` and above

Layout changes:
- Single column on mobile → Two columns on desktop (gallery + details)
- Smaller touch targets on mobile → Larger on desktop
- Adjusted spacing and typography for each screen size

## 🎨 Customization

### Product Data
Edit the `productData` object in `product-page.html`:
```javascript
const productData = {
  title: "Your Product Name",
  images: [/* your image URLs */],
  basePrice: 99.99,
  flavors: ["Flavor1", "Flavor2", "Flavor3"],
};
```

### Pricing
Adjust discount percentages in `updatePricing()`:
```javascript
const subscriptionDiscount = 0.25; // 25% off
const salesDiscount = 0.2;         // 20% off
```

### Tailwind Configuration
Customize colors, fonts, and spacing in `tailwind.config.js`

## 🔄 State Management

The app uses a simple state object to track:
- Current image index
- Purchase mode (single/double)
- Selected flavors per subscription type

```javascript
state = {
  currentImageIndex: 0,
  purchaseMode: "single",
  selectedFlavors: {
    "flavor-1": null,
    "flavor-2": null,
  },
};
```

## ⚡ Performance

- Lightweight vanilla JavaScript (no frameworks)
- CSS animations for smooth transitions
- Optimized images using placeholder URLs
- Mobile-first responsive design
- Fast load time with Tailwind CDN

## 📝 JavaScript Functions

| Function | Purpose |
|----------|---------|
| `init()` | Initialize page and attach event listeners |
| `updateUI()` | Update all UI elements based on state |
| `addToCart()` | Validate and add item to cart |
| `selectFlavor()` | Handle flavor selection |
| `updatePricing()` | Calculate and display prices |
| `showToast()` | Display notification messages |

## 🔧 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

This project is ready for commercial use. Customize for your brand.

## 🤝 Next Steps

1. Replace placeholder images with actual product photos
2. Update product title, description, and pricing
3. Customize flavor options and colors
4. Integrate with your Shopify store backend
5. Add analytics and tracking
6. Set up payment processing

---

**Created**: January 2026  
**Project Type**: Shopify Product Page Template  
**Status**: Ready for deployment



