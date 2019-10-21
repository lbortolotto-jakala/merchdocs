---
title: Creating an Alias Amazon Seller SKU
---


An Alias Amazon Seller SKU is used to create a new Amazon listing from same product in your Magento catalog. If you are an experienced Amazon seller, you may be familiar with the [Amazon Global SKU][1]{: target="_blank"} and Marketplace-specific SKU for inventory and shipping. Following similar principles for Amazon Sales Channel, the Amazon Seller SKU controls product listing information at multi-regional level, and the Alias Amazon Seller SKU can be used to control product listing information at a region-specific level.

This function can be used to perform two functions:

- Create an Alias Amazon Seller SKU for one of your Magento catalog products to control region-specific listing information<br />
<br />**Example**: You are a seller in both the US and the Canada regions. Remember, each of your Amazon Sales Channel stores can only be assigned one Amazon region during setup. This means that you have an Amazon Sales Channel store with a defined US region and another store with a defined Canada region. Both stores share your Magento catalog for listing information across both regions, including the Amazon Seller SKU and ASIN product attributes. So, listings for the catalog product would be the same in both stores, sharing pricing, stock/quantity, and other product attributes. But, your stock for your Canada store ships from a Canada location, and your US store ships from a US location. Thus, you need to control the listing quantity for the listing separately for each store. To accomplish this type of region-specific control, you can create an Alias Amazon Seller SKU.<br />
<br />Essentially, you can create an Alias Amazon Seller SKU that is linked to the same catalog product and can be used to republish the same listing in that region.

- Create an Alias Amazon Seller SKU and match one of your Magento catalog products to two Amazon listings<br />
<br />**Example**: You have a catalog product that is matched to an Amazon listing. As Amazon frequently has multiple listings that represent the same product, you discover another Amazon listing for the same product, but Amazon has assigned a different ASIN to the listing. To increase your product visibility to include, you want to match your catalog product to the different ASIN and create listings for both ASIN values. To accomplish this, you can create an Alias Amazon Seller SKU.<br />
<br />Essentially, you can create an Alias Amazon Seller SKU that can be used to match a single catalog product to a second Amazon listing and create a new listing for the newly matched ASIN. In this scenario, you would have two Amazon listings for the same catalog product.<br />
<br />After you've created an Alias Amazon Seller SKU, you can use your listing settings, rules, and overrides to control the listing information for the region. Product attributes that can be defined per region for a listing include quantity/stock, fulfillment method, condition, product eligibility, and handling time.

## To create an Alias Amazon Seller SKU to be used for a region-specific purpose

View the listing in one of the Product Listing screens (Inactive, Active, Ineligible, or Ended).

1. In the Action column, click **Create Alias Seller SKU**.

1. For **Assign New Seller SKU**, enter a unique alphanumeric value.
<br />This must be a unique value not used for any other product or alias in your catalog.

1. For **Assign New ASIN**, make no change.
<br />This value auto-populates with the ASIN that is matched to your catalog product. Changing this value will match your catalog product to two Amazon listings based on the ASIN.

1. Toggle the Remove Existing Seller SKU option to Yes or No.

    - **Yes**: Select this option to delete the listing and create a new listing using the new information provided.

    - **No**: Select this option to create a new listing and keep the old listing unchanged.

1. Click <span class="btn">Save Listing Update</span>.

## To create an Alias Amazon Seller SKU to be used to match a single catalog product to two Amazon listings

1. View the listing in one of the Product Listing screens (Inactive, Active, Ineligible, or Ended).

1. In the Action column, click **Create Alias Seller SKU**.

1. For **Assign New Seller SKU**, enter a unique alphanumeric value.
<br />This must be a unique value not used for any other product or alias in your catalog.

1. For **Assign New ASIN**, enter a unique alphanumeric value.
<br />This value auto-populates with the ASIN that is matched to your catalog product. Changing this value will match your catalog product to two Amazon listings based on the ASIN.

1. Toggle the Remove Existing Seller SKU option to Yes or No.

    - **Yes**: Select this option to delete the listing and create a new listing using the new information provided.

    - **No**: Select this option to create a new listing and keep the old listing unchanged.

1. Click <span class="btn">Save Listing Update</span>.

![]({% link images/images/sales-channels/amazon/amazon-alias-sku-create.png %}){: .zoom}
_Create an Alias Amazon Seller SKU_

|Field|Description|
|--- |--- |
|Assign New Seller SKU|Enter a new, unique alphanumeric value to be linked to the original Amazon Seller SKU. This number is only used by Amazon Sales Channel to match to your catalog product. You can use any SKU value, but the value can only be used once in your catalog. |
|Assign New ASIN|Enter the ASIN value for the listing to which you want to match your catalog product. Only modify this field when matching a single catalog product to the ASIN for another listing for the same product. This value must match the ASIN assigned by Amazon or the listing will not be rejected by Amazon. |
|Remove Existing Seller SKU|Options:<br/>**Yes**: Select this option to delete the listing and create a new listing using the new information provided. The new listing will display in the Active tab, and the old listing will move to the Ended tab.<br/>**No**: Select this option to create a new listing and keep the old listing unchanged. Both listings will display in the Active tab once the new listing is created. |

[1]: https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090&amp;language=en_US&amp;ref=efph_201394090_cont_G201062890
