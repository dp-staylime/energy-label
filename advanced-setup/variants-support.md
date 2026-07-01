# Variants Support

The app fully supports Shopify variants, allowing you to display a **variant-specific** energy class badge, full energy label, and product information sheet \*\*\*\*based on the selected option.

To enable this, simply add the **EPREL Registration Number** to the relevant **variant metafield** in your Shopify admin:

1. In your Shopify admin, go to **Products**.
2. Create variants or open an existing variant.
3. For each variant, locate the **EPREL Registration Number** metafield.
4. Enter the correct EPREL number and click **Save**.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" icon="triangle-exclamation" %}
**Important notes:**

1. Variant-based energy badges appear only on:

* Product pages
* Cart drawer
* Cart page

Variant-specific badges **do** **not** appear on:

* Collection pages
* Search results

These templates typically use 'Color' as a swatch option and don’t reflect variant-level energy efficiency.

If you want energy badges to show in **Collection** and **Search**, we recommend also setting the **EPREL Registration Number** at the **product level**. This way:

* **Product-level badge** → visible in Collection and Search
* **Variant-level badge** → shown on the Product page, in the Cart drawer, and in the Cart after a variant is selected

2\. [Manual Efficiency Class for Legacy Products](manual-efficiency-class-for-legacy-products.md) feature **is not** supported for variants.
{% endhint %}
