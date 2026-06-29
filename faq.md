# FAQ

{% hint style="info" %}
European Commission services in charge of the Energy labelling product registry, (EPREL), hold all rights, titles and interests in and to the API and/or data, including any copyrights. The energy labels, energy class badges, product information sheets and associated data are provided on an “as is” basis with no guarantees of completeness, accuracy, usefulness or timeliness.
{% endhint %}

<details>

<summary><strong>How do I find the EPREL number for my products?</strong></summary>

There are three ways to locate it:

1. Ask your supplier or manufacturer — they are required to provide the EPREL number.
2. Scan the QR code on the product’s printed or digital energy label — it links to the EPREL page, where the number appears in the breadcrumb as gray digits.
3. Find the EPREL numbers online in the [EPREL database](https://eprel.ec.europa.eu/screen/home). The EPREL number appears as **gray digits in the breadcrumbs** on the product page.

</details>

<details>

<summary><strong>Can the app use GTIN to fetch energy labels and product sheets?</strong></summary>

Not yet. The app currently relies on the EPREL registration number. GTIN support is planned for 2025, once EPREL enables it through their updated API.

</details>

<details>

<summary><strong>Can I manually set the energy class, label, and product sheet without using EPREL?</strong></summary>

Yes, if a product isn’t listed in the EPREL database, you can simply **fill out three metafields** on the product level:

* **Energy Class** (A+++ to G)
* **Energy Label** (image file)
* **Product Information Sheet** (PDF)

There’s no special setting to activate — just enter the data, and the app will display it automatically.

</details>

<details>

<summary><strong>Does the app work with native Shopify variants?</strong></summary>

Yes, it fully supports Shopify variants. To show energy labels per variant, simply use the EPREL Registration Number metafield at the variant level. The app will automatically display the correct badge and product sheet for each one.

</details>

<details>

<summary><strong>Can the app automatically send EPREL data to Google Shopping?</strong></summary>

No — it’s not handled by our app automatically, since merchants use different feed generators.&#x20;

Google requires that the feed includes a special attribute `[certification]`, as outlined here: [Google Merchant Center Certification Attribute Requirements](https://support.google.com/merchants/answer/13528839).&#x20;

You can extract the EPREL number directly from the EPREL Registration Number metafield provided by our app.&#x20;

In short, for each product, the feed should include a certification attribute. You can extract the necessary EPREL number directly from the EPREL Registration Number metafield provided by our app.&#x20;

If your current product feed solution supports custom attributes, you should be able to include this data yourself and stay fully compliant with EU regulations. If not — or if you’re unsure — we’d be happy to explore a custom integration for you.

</details>

<details>

<summary><strong>Can the app use EPREL numbers from another metafield?</strong></summary>

At this time, the app does not support connecting to custom metafields for EPREL numbers. However, there’s a simple workaround: you can **migrate the data from your existing metafield to the app’s required metafield** using third-party tools such as [Matrixify](https://apps.shopify.com/excel-export-import).&#x20;

This allows you to reuse existing EPREL values without manually re-entering them for every product or variant.

</details>

<details>

<summary><strong>What themes does the app support?</strong></summary>

The app supports most themes available at [Shopify Theme Store](https://themes.shopify.com/). However, we cannot guarantee compatibility with custom themes developed by third-party providers or highly customized ones.

</details>
