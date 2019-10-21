---
conditions: Default.B2B Only
title: Set Pricing and Structure
---

Setting up the pricing and structure of a shared catalog is a two-step process. Your current place in the process is highlighted with a number in the progress bar at the top of the page. You can view the other step in the process at any time by clicking the progress bar. For example, if you’re working on custom pricing, you might want to return to the product selection page for reference. Simply click “Products” in the progress bar at the top of the page. Then click “Pricing” to return to the custom pricing page. You will not lose any of your work.

![]({% link images/images-b2b/catalog-shared-products-in-catalog-workspace.png %}){: .zoom}
*Products in Catalog*

In the standard category tree, the root category is the topmost container, and is referred to as “Default Category” in the sample data. However, when shared catalogs are enabled, the category tree has an additional outer container called “Root Catalog.” The root catalog encompasses all other category structures that exist in the system. To learn more, see [Catalog Scope]({% link catalog/catalog-scope.md %}).

## To set up catalog pricing and structure:

1. On the Admin sidebar, tap **Catalog**. Then, choose **Shared Catalogs**.

1. Find the catalog in the [grid]({% link stores/admin-grid-controls.md %}). Then in the **Action** column, select **Set Pricing and Structure**.

1. The first time the shared catalog is configured, tap <span class="btn">Configure</span> to continue. Then, complete the following:

## Step 1: Choose the Products

The first step in the process is to choose the products that you want to include in the shared catalog. The product selection page features the [category tree]({% link catalog/category-create.md %}) on the left, and a synchronized product grid on the right. If you click a category in the tree, the products in the category appear in the grid.

Only categories with selected products appear in the [top navigation]({% link catalog/navigation-top.md %}) when the shared catalog is viewed from the storefront. By default, only the first three [category levels]({% link catalog/navigation-top.md %}) are included in the storefront navigation, not including the root category.

1. Use the **Store** chooser to set the [scope]({% link catalog/product-scope.md %}) of the configuration.

    The scope of the configuration can be set only before the shared catalog is saved for the first time. If you later edit the product selection, the Store chooser is not available.

    ![]({% link images/images-b2b/catalog-shared-products-step1-scope.png %}){: .zoom}
    *Choose Store*

1. In the category tree, do any of the following:

    * To include all products, click **Select all**, or mark the checkbox of the parent category.
    * To include specific categories of products, mark the checkbox of each category that you want to include.
    * To include or exclude an individual product, mark, or clear, the checkbox of product.

    The notation below each category in the tree shows the number of products from the category that are currently included in the shared catalog. The notation below the [root category]({% link catalog/category-root.md %}) shows the total number of products from all categories that are currently selected for the shared catalog.

1. To view category products in the grid, click the name of the category in the tree. When a category is selected, the following occurs:

    * The toggle in the first column of the grid is set to the green “On” position for each selected product.
    * If a product is assigned to multiple categories, and is deselected in one of them, it will continue to be available through the other categories, and also when using [catalog search]({% link catalog/search.md %}).
    * The system automatically sets [Category Permissions]({% link catalog/category-permissions.md %}) to “Allow” for the selected products.

1. If necessary, use the filters and other [grid controls]({% link stores/admin-grid-controls.md %}) to find the products that you want to include in the shared catalog.

    You can individually select, or deselect, individual products by clicking the toggle in the first column.

    If you select a category that has no products, but is linked to CMS content or an external link, it will be included in the top navigation that is visible to customers from the storefront.

    The category settings you make aren’t permanently recorded in the database until the configuration is saved. However, they are saved temporarily as you work on the structure and pricing.

1. Click **Next**.

    ![]({% link images/images-b2b/catalog-shared-choose-products-step1.png %}){: .zoom}
    *Step 1: Select Products for Catalog*

## Step 2: Set Custom Prices

You can set custom pricing for each product individually, or use the Action control to set custom pricing as a fixed amount or percentage for multiple product records.

| Fixed | Specifies the final product price. For example, if you enter a fixed price of $10.00, the price in the storefront for the corresponding company is $10.00. |
| Percentage | Determines the custom price based on the discount percent. For example, to offer a 10 percent discount, set the custom price type to “Percentage,” and enter 10. The discounted custom price is 90 percent of the original product price. |

Use the Custom Price column of the grid to set the discount to a fixed amount or a percentage for the following product types:

* [Simple]({% link catalog/product-create-simple.md %}) (including configurable product variations)
* [Bundle]({% link catalog/product-create-bundle.md %})
* [Downloadable]({% link catalog/product-create-downloadable.md %})
* [Virtual]({% link catalog/product-create-virtual.md %})

The Custom Price column is blank for [configurable]({% link catalog/product-create-configurable.md %}) and [grouped]({% link catalog/product-create-grouped.md %}) products types, and [gift cards]({% link catalog/product-gift-card.md %}).

The selection of products in the grid cannot be changed from the Custom Prices page. However, you can use the progress indicator at the top of the page to return to the previous step and change the selection of products.

## Apply a Custom Price

1. For a multisite installation, set the **Website** chooser to the website where the custom prices apply.

    ![]({% link images/images-b2b/catalog-shared-scope-pricing-step2.png %}){: .zoom}
    *Choose Website*

1. Use one of the following methods to select the products where the custom pricing is to apply.

    * Use the category tree to select all products in a specific category.
    * Set the Mass Actions control in the header to “Select All”
    * Mark the checkbox of individual product(s).

    The grid displays the products in the currently selected categories, and you can use the [standard controls]({% link stores/admin-grid-controls.md %}) to find products and filter the list.

    ![]({% link images/images-b2b/catalog-shared-custom-pricing-mass-actions.png %}){: .zoom}  
    *Select All*

1. Set the **Actions** control to one of the following:

    | Set Discount | Applies a discount percent to all selected products. |
    | Adjust Fixed Price | Applies a fixed price to all selected products. |

    ![]({% link images/images-b2b/catalog-shared-set-custom-prices-discount.png %}){: .zoom}
    *Actions Control - Set Discount*

1. When prompted, enter the discount and tap **Apply**.

    ![]({% link images/images-b2b/catalog-shared-set-custom-prices-actions-set-discount.png %}){: .zoom}
    *Set Discount*

    The discount is applied to all selected products, and the Custom Price column reflects the type of discount and amount applied.
   
    ![]({% link images/images-b2b/catalog-shared-set-custom-prices-actions-set-discount-applied.png %}){: .zoom}
    *Custom Price Column with Discount*

1. When the custom pricing is complete, tap <span class="btn">Generate Catalog</span>. Then, tap <span class="btn">Save</span>.

## Apply a Tier Price

[Tier pricing]({% link catalog/product-price-tier.md %}) lets you offer a quantity discount for products in the shared catalog. The Tier Price column of the grid contains a link to the Advanced Pricing options that apply specifically to the shared catalog. If the product already includes tier pricing, the number of existing tiers appears in parentheses after the link.

The following instructions show how to apply tier pricing to a single product. To apply tier pricing to multiple products, see: [Importing Tier Prices]({% link system/data-import-price-tier.md %}).

1. Find the product in the grid. Then in the **Tier Price** column, click **Configure**.

    ![]({% link images/images-b2b/catalog-shared-tier-price-configure.png %}){: .zoom}
    *Configure Tier Price*

1. On the Advanced Pricing page, tap <span class="btn">Add Price</span>. Then, do the following:

    ![]({% link images/images-b2b/catalog-shared-tier-price-configure-add-price.png %}){: .zoom}
    *Catalog and Tier Price*

    * Choose the **Website** where the tier price applies.
    * Enter the quantity of the product that must be purchased to receive the discount.
    * Set **Price** to one of the following discount types:
        * Fixed
        * Discount
    * Enter the amount of the discount.
    * To enter another tier, tap <span class="btn">Add Price</span>. Then, repeat the process.

    ![]({% link images/images-b2b/catalog-shared-tier-price-configure-multiple-tiers.png %}){: .zoom}
    *Multiple Tier Prices*

1. When complete, tap <span class="btn"> Done</span>.

    In the grid, the number of tiers is shown in parentheses in the Tier Price column.

    ![]({% link images/images-b2b/catalog-shared-tier-price-configure-parentheses.png %}){: .zoom}
    *Multiple Tiers*

The shared catalog is now saved to the database. Its name appears in the Shared Catalog column of the Products grid. The next step is to assign the shared catalog to a company.
