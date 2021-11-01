# Dynamic Products Example

This example demonstrates how you can link a [Product List](https://reflowhq.com/docs/product-list.html) and a [Product](https://reflowhq.com/docs/product.html) component together, so that clicking an item in the list leads you to a full product page.

## How it works

* Product List has the `data-reflow-product-link` attribute set to `./product.html?product={id}`. This instructs Reflow to wrap each list item in a link, and replace the `{id}` placeholder with the actual product id.
* The product page looks for the `product` query parameter, and sets the `data-reflow-product` attribute on the tag on page load.