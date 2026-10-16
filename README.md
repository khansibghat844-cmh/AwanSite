# Awan Mobiles — VS Code Website Project

A responsive, static smartphone catalogue for Awan Mobiles. It contains 57 product listings across Samsung, OPPO, TECNO, iPhone, vivo, Infinix, realme and Xiaomi.

## Open in VS Code
1. Extract this ZIP file.
2. Open VS Code and choose **File → Open Folder**.
3. Select the `awan-mobiles-vscode` folder.
4. Open `index.html` in a browser, or use the VS Code **Live Server** extension and click **Go Live**.
5. Keep all six website files in the same folder.

No build tools or package installation are required. An internet connection is needed for remote product images and web fonts.

## Files
- `index.html` — home page, search, brand filters and catalogue
- `product.html` — product detail page template
- `products.js` — catalogue data for 57 models, variant and colour options, image URLs and specification fields
- `script.js` — catalogue search, sorting, filtering and cards
- `product-detail.js` — variant/colour selection, product details and WhatsApp enquiry link
- `styles.css` — responsive styling

## Before publishing
- **Product data needs final verification.** The catalogue includes data and reference URLs from the working draft; prices and specifications can change and regional variants differ. Confirm every listing against the exact Pakistan-market model/SKU before using it for sales.
- Some models have one product image even though multiple colours are listed. The colour selector updates the selected colour in the WhatsApp enquiry. A colour-specific image will only display if a verified URL is added to that product's `colorImages` map in `products.js`; do not treat a generic image as proof of the selected colour.
- Variant prices update only for entries explicitly present in `variantPrices`. Other variants display “Price to confirm” instead of inventing a price.
- PTA status, live stock and warranty are not connected to a live shop inventory system. Confirm each with the shop.
- Replace `923XXXXXXXXX` at the top of `script.js` and `product-detail.js` with the shop's WhatsApp number (country code + number, digits only). Example format: `923001234567`.
- Review all externally hosted image URLs; they can change or stop working.

## Add verified colour-specific images
Inside a product object in `products.js`, add a `colorImages` object using exact colour labels from that product's `colors` array, for example:

```js
"colorImages": {
  "Black": "https://example.com/verified-black-image.jpg",
  "Green": "https://example.com/verified-green-image.jpg"
}
```

Use only direct image URLs that show the exact model and colour. If a colour is not mapped, the page keeps the model's default image and shows a note that a colour-matched photo is not yet verified.

## GitHub Pages
This is a static site and can be hosted on GitHub Pages. Upload the contents of this folder to a repository, then enable **Settings → Pages** and select the branch/folder where `index.html` is stored.


## Product data review (16 October 2026)

The catalogue contains 57 models and expanded model-specific display, chipset/CPU/GPU, battery/charging, camera, network/connectivity, SIM and extra-feature fields. Internal research links are in `SPEC_RESEARCH_NOTES.md` and are not displayed to customers. Prices, stock, PTA approval and exact Pakistan SKU/variant should be reconfirmed before going live. A field that varies by region is explicitly described as such rather than guessed.


## Product data review (16 October 2026)

The catalogue contains 57 models and expanded model-specific display, chipset/CPU/GPU, battery/charging, camera, network/connectivity, SIM and extra-feature fields. Internal research links are in `SPEC_RESEARCH_NOTES.md` and are not displayed to customers. Prices, stock, PTA approval and exact Pakistan SKU/variant should be reconfirmed before going live. A field that varies by region is explicitly described as such rather than guessed.
