---
description: >-
  Display energy badges across key touchpoints — like Collections, Search, and
  Cart — to help customers preview energy info and ensure full compliance with
  EU Regulation 2017/1369.
---

# Advanced setup

After completing the steps in the [Getting started guide](../getting-started.md), you can configure the app to display clickable energy badges beyond the Product page — on **Collection**, **Search**, **Cart**, and **Cart drawer** templates.

This allows your customers to preview energy efficiency information in their shopping journey, and ensures full compliance with EU Regulation 2017/1369 across all key storefront touchpoints.

## 1. How it works

***

To display energy badges in the correct place on each template, the app relies on **CSS selectors** to:

* Identify the **product container** (product card).
* Place the energy badge **under** the right element (e.g. price, title).

You’ll need to inspect your theme’s HTML structure and define these selectors in the **App embed settings**.

### **How to identify a CSS selector in your theme**

To display the Energy Badge on templates like **Collection**, **Search**, **Cart**, and **Cart drawer**, you’ll need to define the correct CSS selector for where the badge should appear.

Here’s a simple step-by-step guide to finding that selector in your theme using your browser:

1. **Open your storefront.** Go to your live storefront and open the page where you want the Energy Badge to appear — for example, a **Collection** page.
2.  **Right-click the part of the page where the badge should show.** Find the product card or element where you want the Energy Badge to appear (e.g., below the price or product title), then:

    * **Right-click** that area
    * Choose **Inspect** (in Chrome) or **Inspect Element** (in Safari or Firefox)

    This will open the browser’s **developer tools** and highlight the code for that section.
3.  **Look for the class name.** In the HTML code, look for a `class="..."` line that describes the section where you want the badge to appear. For example:<br>

    ```html
    <div class="card__information">
    ```

    \
    Here, `card__information` is the CSS class name you need.
4. **Copy the selector.** To use this class in the app settings copy and paste that into the **Collection**, **Search**, etc., in the Energy Label app embed settings.
5. **Adjust the placement with style settings.** Once you see the badge on the page, use the app’s **style settings** to fine-tune its size, alignment, and spacing to better match your store’s design.

### **Where to enter these settings**

1. Go to **Online Store → Themes → Edit theme**
2. In the editor, click the **App embeds** icon on the left.
3. Locate **EU Energy Label** and toggle it **on**.
4. Scroll down to the **Collection**, **Search**, **Cart**, and **Cart drawer** settings.
5. Paste the selectors into the appropriate fields.
6. Click **Save**.

{% hint style="warning" icon="lightbulb" %}
For **Dawn v15.3.0**, we’ve pre-tested and validated the configuration below.
{% endhint %}

{% columns %}
{% column %}
<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

## 2. Example: Setting up selectors in Dawn theme v15.3.0

### Collection and Search

| **Setting**               | **Value**           |
| ------------------------- | ------------------- |
| Product card CSS selector | `grid__item`        |
| Energy badge CSS selector | `card__information` |

To display the energy badge in the right place, find the CSS selectors in your theme and insert them in the following settings:

* **Product card CSS selector**: this targets the **product card** element within the grid.
* **Energy badge CSS selector**: this targets the element **under** which the Energy Badge will be displayed.

By using the correct selectors, you ensure the Energy Badge appears in the desired location within your store’s **Collection** template.

The following screenshot highlights the CSS selector of a product card (`grid__item`) within the product grid. Specifically, the selector shown is for a list item (`li`). Usually, this element is part of a product grid structure. This selector should be used to target the product card.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

The following screenshot highlights the CSS selector of the product’s information block (`card__information`) inside the product card **under** which you would like to display the Energy Badge. After identifying this selector, you should use it in the configuration settings to properly position the Energy Badge.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

In our case, the **Search** template shares the same structure as **Collection**, so we use the same selectors. If your theme uses a different layout for search results, follow the same process as described above to inspect the HTML structure and define the correct selectors.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

Once the Energy Badge is successfully displayed on these templates, you can use the style settings (size, alignment, horizontal and vertical margins) to adjust its appearance to better match your store’s layout and design preferences.

### Cart

| **Setting**               | **Value in Dawn v15.3.0** |
| ------------------------- | ------------------------- |
| Product card CSS selector | `cart-item`               |
| Energy badge CSS selector | `product-option`          |

To display the energy badge in the correct place, find the relevant CSS selectors in your theme and insert them into the following settings:

1. **Product card CSS selector**: this targets the **product card** element within the cart.
2. **Energy badge CSS selector**: this targets the element **under** which the Energy Badge will be displayed in the cart.

By using the correct selectors in these settings, the Energy Badge will be properly positioned in the **Cart** template of your store.

The following screenshot highlights the CSS selector of a product card (`cart-item`) within the product grid.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

The following screenshot highlights the CSS selector of the product’s price (`product-option`) inside the product card **under** which you would like to display the Energy Badge. After identifying this selector, you should use it in the configuration settings to properly position the Energy Badge.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

### Cart drawer

| **Setting**               | **Value in Dawn v15.3.0** |
| ------------------------- | ------------------------- |
| Cart drawer CSS selector  | `cart-drawer`             |
| Product card CSS selector | `cart-item`               |
| Energy badge CSS selector | `product-option`          |

Since the **Cart drawer** is not a standalone template in Shopify themes, but rather a component embedded into the theme, the process differs slightly from the others. Here’s how to configure it properly.

**Step 1: Make sure your theme supports a cart drawer**

{% stepper %}
{% step %}
#### **Step 1: Make sure your theme supports a cart drawer**

Before configuring the Energy Badge display in the cart drawer, please ensure that your theme includes this feature. Some themes may not support a cart drawer by default and instead use a traditional cart page.

In **Dawn**, for example, you can enable the cart drawer by navigating to:

**Online store → Themes → Customize → Theme settings → Cart → Type**, and selecting **Drawer:**

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" icon="triangle-exclamation" %}
**Please note:** the exact location of this setting may vary depending on your theme. If you don’t see the option, your theme may not support a cart drawer out of the box.
{% endhint %}
{% endstep %}

{% step %}
#### **Step 2: Add a product to your cart**

In order to inspect the cart drawer HTML structure, open your storefront in a new browser tab and add at least one product to the cart. This will allow the cart drawer to appear and the relevant HTML to be loaded into the DOM.
{% endstep %}

{% step %}
#### **Step 3: Inspect the cart drawer structure**

To display the Energy Badge correctly inside the cart drawer, you first need to identify and set the CSS selector for the **cart drawer wrapper itself**. This is a required field that tells the app where to look for product cards inside the drawer.

You can locate the correct selector by inspecting the cart drawer’s outer container. In the **Dawn v15.3.0** theme, the appropriate selector is `cart-drawer`:

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

Once this is configured, you can define the remaining selectors — **Product card CSS selector** and **Energy badge CSS selector** — the same way as described earlier for the **Cart** template.

In our case (Dawn v15.3.0), the same selectors used for the **Cart** template also apply to the **Cart drawer**, so we reused them. If your theme uses a different structure, follow the same steps as outlined above to define selectors for your drawer setup.
{% endstep %}
{% endstepper %}
