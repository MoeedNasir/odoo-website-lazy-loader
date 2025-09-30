# Website Product Lazy Load

Enhance your eCommerce shopping experience with seamless product loading. This Odoo module eliminates traditional pagination by implementing lazy loading functionality for website products.

## Features

- **Multiple Loading Options**: Choose from button click or infinite scroll loading
- **Multilingual Support**: Works seamlessly with all languages (English, Arabic, etc.)
- **Performance Optimized**: Loads products on demand for faster initial page loads
- **Mobile Friendly**: Responsive design works on all devices
- **Easy Configuration**: Switch between loading modes via website editor

## Installation
1. Install the module through Odoo Apps or manually:
   ./odoo-bin -d your_database -u wt_website_product_lazy_load
Restart your Odoo server after installation

**Configuration**

**Method 1: Website Editor**
Go to your website shop page
Enter Edit mode
Click "Customize" in the top toolbar
Under the "Pagination" section, choose your preferred loading method:
Default: Traditional pagination
Button: Load more products with a button click
Scroll: Infinite scroll loading

**Method 2: Technical Configuration**
The module automatically handles:
Language-specific routes (/en/shop, /ar/shop, etc.)
Product category pages
Search and filter results
Price range filtering
Technical Details
Supported Routes
/shop
/shop/page/<page>
/shop/category/<category>
/ar/shop (and other language prefixes)
/ar/shop/page/<page>
/ar/shop/category/<category>
API Endpoints
POST /shop-lazy/page/<page>
POST /<lang>/shop-lazy/page/<page>

**JavaScript Integration**
The module uses vanilla JavaScript with:
Fetch API for AJAX requests
Intersection Observer pattern for scroll detection
Debounced scroll events for performance
Bootstrap 5 compatible UI components

**Files Structure**

wt_website_product_lazy_load/
├── __manifest__.py
├── controllers/
│   └── main.py
├── static/
│   └── src/
│       └── js/
│           └── lazy_load.js
├── views/
│   ├── website_sale_templates.xml
│   └── snippets.xml
└── README.md

**Dependencies**
Odoo 18.0+
website_sale module

**Support**
For technical support or feature requests, contact:
Email: moeednasir342@gmail.com
Website: https://moeed-portfolio.netlify.app/

**License**
This module is licensed under OPL-1 (Odoo Proprietary License v1.0).

**Version**
Current Version: 18.0.0.0.1

**Changelog**
Version 18.0.0.0.1
Initial release



