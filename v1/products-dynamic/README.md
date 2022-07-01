# Dynamic Products Example

This example demonstrates how to link components together to create a fully featured store with products, categories and a shopping cart.

## Dynamic Products

The [Products](https://reflowtoolkit.github.io/examples/v1/products-dynamic/index.html) example demonstrates how you can link a [Product List](https://reflowhq.com/docs/product-list.html) and a [Product](https://reflowhq.com/docs/product.html) component together, so that clicking an item in the list leads you to a full product page.

### How it works

* Product List has the `data-reflow-product-link` attribute set to `./product.html?product={id}`. This instructs Reflow to wrap each list item in a link, and replace the `{id}` placeholder with the actual product id.
* The product page looks for the `product` query parameter, and sets the `data-reflow-product` attribute on the tag on page load.

## Dynamic Categories

In the [Categories](https://reflowtoolkit.github.io/examples/v1/products-dynamic/categories.html) example you can learn how to connect a [Category List](https://reflowhq.com/docs/category-list.html) and a [Product List](https://reflowhq.com/docs/product-list.html) component together. This creates a navigation menu for browsing all categories and products from the store.

### How it works

* Category List has the `data-reflow-category-link` attribute set to `./index.html?category={id}` (the product list example page). This instructs Reflow to wrap each list item in a link, and replace the `{id}` placeholder with the actual category id.
* The product list page looks for the `category` query parameter, and sets the `data-reflow-category` attribute on the tag on page load. It then lists all products from the specified category.

## Shopping Cart

The [Cart](https://reflowtoolkit.github.io/examples/v1/products-dynamic/cart.html) example displays a shopping cart where you can see all the [Products](https://reflowhq.com/docs/product.html) that were added for purchase.

### How it works

* The Product component has the `data-reflow-shoppingcart-url` attribute set to `./cart.html`.
* This links the components together, so that when the **Add to Cart** button is pressed products are correctly added for purchase.