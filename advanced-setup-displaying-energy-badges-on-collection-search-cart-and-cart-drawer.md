# Advanced setup: displaying Energy Badges on Collection, Search, Cart, and Cart drawer

This allows your customers to preview energy efficiency information in their shopping journey, and ensures full compliance with EU Regulation 2017/1369 across all key storefront touchpoints.



### Supported page types



The table below shows which page types display the energy badge and how they are configured:



Page type | Badge display | Configuration required

-— | -— | ---

Product page | Always shown when EPREL is set | None — works automatically

Collection page | Shown when CSS selectors are set | Required

Search results | Shown when CSS selectors are set | Required

Cart page | Shown when CSS selectors are set | Required

Cart drawer | Shown when CSS selectors are set | Required

Home page | Not supported out of the box | Contact support for paid customization



> **Note:** CSS selector configuration is required for all page types except Product page. If you skip this step, badges will only appear on the Product page.



### 1. How it works



To display energy badges in the correct place on each template, the app relies on **CSS selectors** to:



* Identify the **product container** (product card).
* \- Place the energy badge **under** the right element (e.g. price, title).

You’ll need to inspect your theme’s HTML structure and define these selectors in the **App embed settings**.



#### How to identify a CSS selector in your theme



1. **Open your storefront.** Go to the page where you want the Energy Badge to appear (e.g. a Collection page).
2. 2\. **Right-click** the part of the page where the badge should show. Choose **Inspect** (Chrome) or **Inspect Element** (Safari/Firefox).
3. 3\. **Look for the class name.** In the HTML code, find a `class="..."` line that describes the section. For example: `<div class="card__information">`
4. 4\. **Copy the selector** and paste it into the Energy Label app embed settings.
5. 5\. **Adjust placement** with the app’s style settings (size, alignment, spacing).

#### Where to enter these settings



1. Go to **Online Store → Themes → Customize**.
2. 2\. Click the **App embeds** icon on the left.
3. 3\. Locate **EU Energy Label** and toggle it on.
4. 4\. Scroll down to the Collection, Search, Cart, and Cart drawer settings.
5. 5\. Paste the selectors into the appropriate fields. Click **Save**.

### 2. Example: Setting up selectors in Dawn theme v15.3.0



#### Collection and Search



\| Setting | Value |

\|---------|-------|

\| Product card CSS selector | `grid__item` |

\| Energy badge CSS selector | `card__information` |



For Collection and Search templates in Dawn, use the same selectors. If your theme uses a different layout for search results, follow the CSS inspection steps above.



#### Cart



\| Setting | Value in Dawn v15.3.0 |

\|---------|----------------------|

\| Product card CSS selector | `cart-item` |

\| Energy badge CSS selector | `product-option` |



#### Cart drawer



\| Setting | Value in Dawn v15.3.0 |

\|---------|----------------------|

\| Cart drawer CSS selector | `cart-drawer` |

\| Product card CSS selector | `cart-item` |

\| Energy badge CSS selector | `product-option` |



Before configuring the cart drawer, make sure your theme supports it. In Dawn, enable it via **Online store → Themes → Customize → Theme settings → Cart → Type → Drawer**.



Also, add at least one product to your cart before inspecting the cart drawer HTML, as the drawer only renders when a product is in the cart.



### Compatibility notes



The app has been tested and confirmed to work with the following themes:



* **Dawn** (Shopify default theme, v13+) — fully supported
* \- **Warehouse** — fully supported

If your store uses a custom or third-party theme, CSS selector configuration is required. Themes with non-standard product card structures may need custom selectors.



**Known issues with third-party apps:**



Some third-party search and product filter apps (such as "AI Search & Product Filter" or similar tools) replace the default product container elements with their own HTML. This can prevent the energy badge from appearing on collection and search pages even when selectors are configured correctly.



If badges don't appear after setup and your store uses a third-party filter app, contact support with your theme name, the filter app name, and a link to the affected page.
