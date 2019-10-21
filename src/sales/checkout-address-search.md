---
conditions: Default.EE-B2B
title: Address Search
---

Your customers could have a large number of saved addresses and information in their address book, especially regular, returning customers or companies entering multiple orders and shipment locations. Displaying a large amount of addresses can slow checkout loading and processes considerably, and result in a negative shopping experience. To help increase the responsiveness of checkout, we recommend activating and configuring address search for your site.

{: .bs-callout .bs-callout-info}
Address search is not enabled by default. You must configure this feature to include the functionality on your site.

When this feature is enabled and the customer's number of saved addresses meets or exceeds the configured limit, only one address is displayed (the default address, if the customer has one) for the _Shipping_ and _Review & Payments_ steps. The customer can change the selected address by clicking **Change Address** and then searching for the correct address by city, state, street, or zip. This feature also supports address selection for gift registry checkout.

![]({% link images/images-ee/storefront-checkout-address-search.png %}){: .zoom}
_Select Shipping Address_

If the customer does not have a default shipping address, the Shipping page displays "No address selected" and the customer must click **Change Address** to select a saved address or click <span class="btn">New Address</span> to add and select an address before proceeding with the checkout. If the customer does not have a default billing address, the Review & Payments page displays the address selected for shipping along with the Change Address option.

![]({% link images/images-ee/storefront-checkout-address-search-no-default.png %}){: .zoom}
_No address selected_

<!--{% if "Default.B2B Only" contains site.edition %}-->Enabling address search also affects the checkout for negotiated quotes where customer's number of saved addresses meets or exceeds the configured limit. When the quote is complete and the customer proceeds to the checkout, only the selected shipping address is displayed. The page also displays a message that the shipping address is locked and can only be changed in the quote.

![]({% link images/images-b2b/storefront-checkout-quote-address-limit.png %}){: .zoom}
_Shipping address locked for quote_

<!--{% endif %}-->
## To enable address search:

1. On the _Admin_ sidebar, click **Stores**.

1. In the _Settings_ section, choose **Configuration**.

1. In the _Sales_ section in the left panel, choose **Checkout**.

1. Expand ![]({% link images/images/btn-expand.png %})the **Checkout Options** section.

    ![]({% link images/images-ee/config-sales-checkout-checkout-options.png %}){: .zoom}
    [_Checkout Options_]({% link configuration/sales/checkout.md %})

1. Set **Enable Address Search** to "Yes".

1. Set the **Number of Customer Addresses Limit** option to specify the threshold for including the address search feature.

   If necessary, clear the **Use system value** checkbox to make this change.

   When the customer's number of saved addresses meets or exceeds this limit, the page displays either the default address (if the customer has one) or "No address selected" with the **Change Address** option. The default limit is 10.

1. Click **Save Config**.
