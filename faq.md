# FAQ

### General



### What is the EU Energy Label app?



The EU Energy Label app by Staylime lets you display compliant energy efficiency labels, badges, and product information sheets on your Shopify storefront. It fetches product data automatically from the EPREL database using the product's registration number, and displays the correct label on product pages, collection pages, search results, the cart, and the cart drawer.



### Where does the energy badge appear?



By default, after completing the setup, the energy badge appears on the **Product page**. To show it on Collection pages, Search results, Cart, and Cart Drawer, you need to configure CSS selectors in the Advanced Setup. See \[Advanced setup]\(/advanced-setup-displaying-energy-badges-on-collection-search-cart-and-cart-drawer).



### Can I show the energy badge on my home page?



Home page display is not supported out of the box. The app is designed for product-specific contexts (Product page, Collection, Search, Cart). Displaying badges in homepage sections (e.g., featured collections) requires custom development. Contact support to discuss a paid customization.



### What is EPREL?



EPREL (European Product Registry for Energy Labelling) is the official EU database where manufacturers register energy-related products. Each product gets a unique registration number that the app uses to fetch the correct energy label and product information sheet.



### Where do I find the EPREL Registration Number for my product?



The EPREL Registration Number is provided by the product manufacturer. You can also look it up in the official EPREL database at eprel.ec.europa.eu by searching for your product model.



### Does the app support all Shopify themes?



The app works with most standard Shopify themes. For custom or third-party themes, CSS selector configuration may be required (see Advanced Setup). Some third-party search and filter apps may override product container elements — if badges don't appear after setup, contact support with your theme name and we'll help troubleshoot.



### Does the app work with Online Store 2.0 themes?



Yes. The app supports Online Store 2.0 themes and uses app blocks that can be added via the Shopify theme editor without editing code.



### Support



### Why doesn't the energy label appear on my product page?



The most common reason is that the **EPREL Registration Number** metafield is empty for that product. The app only renders the label when a valid EPREL number is present. Go to your product in Shopify admin, scroll to Metafields, and make sure the EU Energy Label: EPREL Registration Number field is filled in.



### Why does the badge appear on the product page but not on collection / search / cart pages?



These page types require manual CSS selector configuration. After installing the app, go to the app settings and enter the correct CSS selectors for each page type. See \[Advanced setup]\(/advanced-setup-displaying-energy-badges-on-collection-search-cart-and-cart-drawer) for step-by-step instructions.



### The energy label popup looks broken or too small on iPhone / Safari — what should I do?



This is a known display issue that was resolved in a recent app update. Make sure you have the latest version of the app installed. If the issue persists after updating, contact support with your store URL and a screenshot.



### What happens when a customer clicks on the energy badge?



Clicking the badge opens the full energy label in a new browser tab as a PDF or image, depending on what is registered in EPREL for that product.



### I installed the app but the badge block doesn't appear in the theme editor — what should I do?



Make sure the app embed is enabled. Go to your Shopify admin, then **Online Store → Themes → Customize**, click **App embeds** in the left panel, and toggle on the EU Energy Label embed. Then add the EU Energy Label block to your product template.



### My product is not in the EPREL database — can I still show a label?



Yes. Use the Manual Efficiency Class feature. Fill in the Energy Class, Energy Label image, and Product Information Sheet metafields directly on the product, and leave the EPREL Registration Number field empty. See \[Manual Efficiency Class for Legacy Products]\(/manual-efficiency-class-for-legacy-products).



### Does the app support products with variants?



Yes. You can assign a separate EPREL Registration Number to each variant via variant metafields. Note that variant-specific badges appear on Product pages, Cart, and Cart Drawer — but not on Collection or Search pages, which show the product-level badge. See \[Variants Support]\(/variants-support).
