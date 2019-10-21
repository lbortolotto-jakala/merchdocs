---
conditions: Default.EE-B2B
title: Sorting Category Products
---

The position of products in a category can be specified manually by dragging and dropping products into position or by applying a predefined sort order. By default, products can be sorted by stock level, age, color, name, SKU, and price. Automatic sort overrides the current sort order and resets any drag-and-drop positions that were set manually. The sort order of colors and the minimum stock level that can be required for products to be included in the list are set in the [Visual Merchandiser]({% link configuration/catalog/visual-merchandiser.md %}) configuration.

You can set up the category options separately for each [store]({% link stores/stores-all-create-store.md %}) to determine the selection of products, their relative position in the list, and the attributes that are available for category rules. However, only one sort order can be assigned to the [store view]({% link stores/stores-all-create-view.md %}) level of any store.

## Step 1: Set the Scope of the Configuration

1. On the Admin sidebar, choose **Catalog**. Then, choose **Categories**.

1. If necessary, choose the **Store View** where the settings apply.

    For a multistore installation, the Store View setting applies the sort order to all available views within the store.

1. In the category tree on the left, choose the category that you want to edit.

    ![]({% link images/images-ee/category-workspace.png %}){: .zoom}
    *Category Tree*

## Step 2: Sort the Products

In the **Products in Category** section, click the tiles (![]({% link images/images/btn-view-as-tiles.png %}){: .Inline}) button, below the Add Products button, to show the product tiles in a grid. Then, use the **Manual Sort** or **Automatic Sort** method to sort the products:

![]({% link images/images-ee/category-products-tiles.png %}){: .zoom}
*Product Tiles*

   **Method 1: Manual Sort**

   1. Set **Sort Order** to your preference.

   1. Click <span class="btn">Sort</span> to apply the new sort order.

         ![]({% link images/images-ee/category-edit-sort-order.png %}){: .zoom}
         *Sort Order*

   1. To save the sort order, click <span class="btn">Save Category</span>.

   1. When prompted, update any invalid indexers.

   **Method 2: Automatic Sort**

   1. Set **Match products by rule** (![]({% link images/images/btn-switch-yes.png %}){: .Inline}) to “Yes”.

        ![]({% link images/images-ee/category-edit-automatic-sorting.png %}){: .zoom}
        *Match Products by Rule*

   1. Set **Automatic Sorting** to your preference.

   1. Follow the instructions in the next step to create a category rule.

## Step 3: Create a Category Rule

1. Set **Match products by rule** (![]({% link images/images/btn-switch-yes.png %}){: .Inline}) to “Yes”.

1. Click <span class="btn">Add Condition</span>. Then, do the following:

    ![]({% link images/images-ee/category-edit-condition.png %}){: .zoom}
    *Category Condition*

   * Choose the **Attribute** that is the basis of the condition.

   * Set **Operator** to one of the following:

       * Equal / Not equal
       * Greater than / Greater than or equal to
       * Less than / Less than or equal to
       * Contains

   * Enter the appropriate **Value**.

1. To add another condition, click <span class="btn">Add Condition</span> and repeat the process.

## Step 4: Save, Refresh, and Verify

1. When complete, click <span class="btn">Save Category</span>.

1. When prompted to refresh the cache, click the **Cache Management** link and refresh each invalid cache.

1. In the storefront, verify that the product selection, sorting, and category rules work correctly. If you need to make adjustments, change the settings and try again.
