---
description: >-
  Some products may not yet be registered in the EPREL database but still need
  to display an energy efficiency label on your storefront. For these legacy
  products, the app lets you manually specify the
---

# Manual Efficiency Class for Legacy Products

### How it works



Instead of fetching data from EPREL automatically, the app reads from three dedicated product metafields:



* **Energy Class** — the efficiency class letter (e.g., A, B, C, D, E, F, G, A+, A++, A+++)
* \- **Energy Label** — an image of the energy label
* \- **Product Information Sheet** — a PDF file with technical product details

> **Important:** For the manual mode to activate, the **EPREL Registration Number** metafield must be **left empty**. If an EPREL number is present, the app will try to fetch data from the registry instead.

### Setup steps



1. Go to **Products** in your Shopify admin and open the product.
2. 2\. Scroll down to the **Metafields** section.
3. 3\. Fill in the following fields:
4. &#x20;  \- **EU Energy Label: Energy Class** — enter the energy efficiency class (e.g., `A+`)
5. &#x20;  \- **EU Energy Label: Energy Label** — upload the energy label image
6. &#x20;  \- **EU Energy Label: Product Information Sheet** — upload the PDF file
7. 4\. Make sure the **EPREL Registration Number** field is empty.
8. 5\. Click **Save**.

> 📸 SCREENSHOT: Shopify admin — product metafields showing Energy Class, Energy Label image, and Product Information Sheet fields

### Limitations



* Manual Efficiency Class works at the **product level only** — it is **not supported for variants**.
* \- To display variant-specific labels, the product must be registered in EPREL. See \[Variants Support]\(/variants-support).
* Supported page types: Product page, Collection page, Search results, Cart page, and Cart Drawer — same as EPREL-based labels.
