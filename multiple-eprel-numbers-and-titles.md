# Multiple EPREL Numbers & Titles

If a product has multiple energy labels (e.g., for different EU member states or product configurations), you can assign more than one EPREL Registration Number to it.



### Format



Enter multiple EPREL numbers in the **EPREL Registration Number** metafield, separated by commas. Each number can optionally have a custom title in square brackets:



````

number[title], number[title]
```

Examples:

```
12345678[DE], 87654321[FR]
```

```
12345678[Germany], 87654321[France]
```

If no title is provided, the app will display the default label without a custom heading.

> 📸 SCREENSHOT: Product metafield showing multiple EPREL numbers with titles in the format number[title], number[title]

### Limitations

- Multiple EPREL numbers work at the **product level only**.
- This feature is only available on the **Product page** template — not on Collection, Search, Cart, or Cart Drawer.
- For variant-specific labels, each variant needs its own individual EPREL Registration Number. See [Variants Support](/variants-support).
````
