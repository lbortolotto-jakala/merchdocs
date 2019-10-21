---
title: PayPal Payflow Pro
---

{:.bs-callout .bs-callout-warning}
**Payment Services Directive Requirements:** <br/>
As of September 14, 2019, European banks might decline payments that do not meet [PSD2]({% link stores/compliance-payment-services-directive.md %}) requirements. To comply with PSD2, PayPal Payflow Pro must be integrated with Cardinal Commerce. To learn more, see [3-D Secure for Payflow](https://developer.paypal.com/docs/classic/payflow/3d-secure-overview/).

PayPal Payflow Pro gateway, formerly known as Verisign, is available for customers of the United States, Canada, Australia, and New Zealand. Unlike other PayPal payment methods, merchants are charged a fixed monthly fee, plus a fixed fee for each transaction, regardless of their number.

![Checkout with PayPal]({% link images/images/storefront-cart-paypal.png %}){: .zoom}
_Checkout with PayPal_

## Requirements

* [PayPal Business Account][1] The PayPal Payflow Pro gateway links the merchant account at PayPal with the merchant’s website, and acts both as a gateway and a merchant account.  

* If you manage multiple Magento websites, you must have a separate PayPal merchant account for each website.

## Customer Workflow

| **1** | **Customer Goes to Checkout** | During checkout, the customer chooses to pay with PayPal PayFlow Pro, and enters the credit card information.Customers are not required to have personal PayPal accounts. However, depending on the merchant country, customers can also use their personal PayPal account to pay for the order.|
| **2** | **Customer Submits Order** | The customer submits the order, and the order information is sent to PayPal for processing. The customer does not leave the checkout page of your site.|
| **3** | **PayPal Completes the Transaction** | Payments are accepted at the time the order is placed. Depending on the payment action specified n the configuration, either a sales order or a sales order and an invoice is created. |

## Online Order Processing Workflow

| **1** | **Administrator Submits Online Invoice** | The store administrator submits an online invoice. and as a result a corresponding transaction and an invoice is created.|
| **2** | **PayPal Receives the Transaction** | The order information is sent to PayPal. A record of the transaction and an invoice is generated. You can view all Payflow Pro Gateway transactions in your [PayPal merchant account][2].|

{:.bs-callout .bs-callout-info}
Partial invoices and partial refunds are not supported by PayPal Payflow Pro.

## Setting Up PayPal Payflow Pro

### Step 1: Configure Your PayPal Account

Before you begin, set up your PayPal Payments Advanced account on the PayPal website.

1. Log in to your PayPal [business account][2].

   ![PayPal Manager Login]({% link images/images/paypal-manager-login.png %}){: .zoom}
   _PayPal Manager Login_

1. In the PayPal Manager menu, choose **Service Settings**. Under **Hosted Checkout Pages**, click **Set Up**. Then, do the following:

   ![Service Settings]({% link images/images/paypal-manager-service-settings.png %}){: .zoom}
   _Service Settings_

   - Under **Choose your settings**, set **Transaction Process Mode** to “Live”.

   - Under **Display options on payment page**, set **Cancel URL Method** to “POST”.

     ![Display Options on Payment Page]({% link images/images/paypal-manager-service-settings-display-options-payment-page.png %}){: .zoom}
     _Display Options on Payment Page_

   - Under **Billing Information**, mark the card security code **CSC** checkboxes for both required and editable fields.

     ![Billing Information]({% link images/images/paypal-manager-billing-information.png %}){: .zoom}
     _Billing Information_

   - Under **Payment Confirmation**, set **Return URL Method** to “POST”.

     ![Payment Confirmation]({% link images/images/paypal-manager-payment-confirmation.png %}){: .zoom}
     _Payment Confirmation_

   - Under **Security Options**, make the following settings:

     |**AVS** |No |
     |**CSC** |No |
     |**Enable Secure Token** |Yes |

     ![Security Options]({% link images/images/paypal-manager-security-options.png %}){: .zoom}
     _Security Options_

   * When complete, tap <span class="btn">Save Changes</span>.

1. In the PayPal Manager menu, again choose **Service Settings**. Then under **Hosted Checkout Pages**, choose **Customize**, and do the following:

   - Choose **Layout C**.

     ![Customize Your Page]({% link images/images/paypal-manager-service-settings-customize-your-page.png %}){: .zoom}
     _Customize Your Page_

     Layout C shows only credit and debit card fields, and can either be framed on your site or used as a stand-alone popup. The size is fixed at 490 x 565 pixels, with extra space for error messages. On some systems, this setting corrects an issue with transparent redirect.

     ![Layout C Example]({% link images/images/paypal-manager-payflow-pro-layout-c-example.png %}){: .zoom}
     _Layout C Example_

   - Tap <span class="btn">Save and Publish</span>.

1. In the PayPal Manager menu, choose **Account Administration**. Under **Manage Security**, click **Transaction Settings**. Then, do the following:

   - Set **Allow reference transactions** to “Yes”.

   - Tap <span class="btn">Confirm</span>.

     {:.bs-callout .bs-callout-info}
     If you have multiple Magento websites, you must create a separate PayPal Payments Advanced account for each.

1. PayPal recommends that you set up an additional user on your account. To set up an additional user, do the following:

   - In the second row of the main menu, click **Manage Users**.

   - To add another user to the account, click **Add User**. The link is located just above the Manage Users title.

     ![Manage Users]({% link images/images/paypal-manager-manage-users.png %}){: .zoom}
     _Manage Users_

   - Complete the required fields in the following sections of the Add User form:

     - Admin Confirmation
     - User Information
     - User Login Information
     - Assign Privilege to User

   - When complete, tap <span class="btn">Update</span>. Then in the upper-right corner, click **Log Out**.

### Step 2: Complete the Required Settings

1. Return to Magento to complete the required settings. If the [session lifetime]({% link stores/admin-session-lifetime.md %}) timed out while you were working in PayPal Manager, you’ll have to log in again.

1. On the Admin sidebar, tap **Stores**. Then under **Settings**, choose **Configuration**, and do the following:

   - In the panel on the left, under **Sales**, choose **Payment Methods**.

   - If your Magento installation has multiple websites, stores or views, set **Store View** to the store view where the configuration applies.

   - In the **Merchant Location** section, select the **Merchant Country** where your business is located.

     This setting determines the selection of PayPal Solutions that appear in the configuration.

1. Under **PayPal Payment Gateways**, in the **PayPal Payflow Pro** section, tap <span class="btn">Configure</span>.

   ![Configure]({% link images/images/config-sales-payment-methods-paypal-payflow-pro.png %}){: .zoom}
   _Configure_

1. In the **Required PayPal Settings** section under Payments Pro and Express Checkout, do the following:

   - (Optional) Enter the **Email Associated with your PayPal Merchant Account**.

     {:.bs-callout .bs-callout-warning}
     Email addresses are case sensitive. To receive payment, the email address must match the email address specified in your PayPal merchant account.

     If you don’t yet have a PayPal account, click the link, **Start accepting payments via PayPal**.

   - Enter one of the following credentials that you use to log in to your PayPal merchant account:

     | **Partner** | Your PayPal Partner ID.|
     | **User** | The ID of an additional user who is set up on your PayPal account.|
     | **Vendor** | Your PayPal user login name.|

   - Enter the **Password** that is associated with your PayPal account.

   - If you want to run test transactions, set **Test Mode** to “Yes.”

     When testing the configuration in a sandbox, use only [credit card numbers ][3] that are recommended by PayPal. When you are ready to “go live,” return to the configuration and set Test Mode to “No.”

1. If your system uses a proxy server to establish the connection to the PayPal system, set **Use Proxy** to “Yes.” Then, do the following:

   - Enter the IP address of the **Proxy Host**.

   - Enter the port number of the **Proxy Port**.

   A proxy is used when the server firewall prevents direct access to the PayPal server. In such a case, a third-party server is used to relay traffic.

   ![Required Settings]({% link images/images/config-sales-payment-methods-paypal-payflow-pro-required-a.png %}){: .zoom}
   _Required Settings_

1. Set **Enable This Solution** to “Yes.”

1. If you want to offer PayPal Credit to your customers, set **Enable PayPal Credit** to “Yes.”

   ![Enable PayPal Payflow Pro]({% link images/images/config-sales-payment-methods-paypal-payflow-pro-required-b.png %}){: .zoom}
   _Enable PayPal Payflow Pro_

### Step 3: Advertise PayPal Credit (Optional)

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline}the **Advertise PayPal Credit** section. Then, do the following:

   - Tap **Get Publisher ID from PayPal**, and follow the instructions to get your account information.

   - Enter your **Publisher ID**.

     ![Advertise PayPal Credit]({% link images/images/config-sales-payment-methods-paypal-payments-advanced-advertise-paypal-credit.png %}){: .zoom}
     _Advertise PayPal Credit_

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline}the **Home Page** section. Then, do the following:

   - To place a banner on the page, set **Display** to “Yes.”

   - Set **Position** to one of the following:

     - Header (center)
     - Sidebar (right)

   - Set **Size** to one of the following:

     - 190 x 100
     - 234 x 60
     - 300 x 50
     - 468 x 60
     - 728 x 90
     - 800 x 66

   ![Advertise PayPal Credit Home Page Settings]({% link images/images/config-sales-payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png %}){: .zoom}
   _Advertise PayPal Credit Home Page Settings_

1. Repeat the previous step for the remaining sections:

   - Catalog Category Page
   - Catalog Product Page
   - Checkout Cart Page

### Step 4: Complete the Basic Settings

1. In the **Basic Settings - PayPal Payflow Pro** section, enter a **Title** to identify PayPal Payflow Pro during checkout. It is recommended that you use the title “Debit or Credit Card.”

1. If you offer multiple payment methods, enter a number in the **Sort Order** field to determine the sequence in which PayPal Payflow Pro appears when listed with other payment methods during checkout.

1. Set **Payment Action** to one of the following:

   | **Authorization** | Approves the purchase, but puts a hold on the funds. The amount is not withdrawn until it is “captured” by the merchant.
   | **Sale** | The amount of the purchase is authorized and immediately withdrawn from the customer’s account.

1. Under **Credit Card Settings**, select each credit card that you accept for payment in your store. To make multiple selections, hold down the Ctrl key and click each item.

   {:.bs-callout .bs-callout-info}
   American Express requires an additional agreement.

   ![Basic Settings]({% link images/images/config-sales-payment-methods-paypal-payflow-pro-basic-settings.png %}){: .zoom}
   _Basic Settings_

### Step 5: Complete the Advanced Settings

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline}the **Advanced Settings** section. Then, do the following:

   - Set **Payment Applicable From** to one of the following:

     |**All Allowed Countries** |Customers from all [countries]({% link stores/country-options.md %}) specified in your store configuration can use this payment method. |
     |**Specific Countries** |After choosing this option, the Payment from Specific Countries list appears. Hold down the Ctrl key and select each country in the list where customers can make purchases from your store. |

   - Set **Debug Mode** to “Yes” to write communications with the payment system into the log file.

     {:.bs-callout .bs-callout-info}
     In accordance with PCI Data Security Standards, credit card information is not recorded in the log file.

   - To enable host authenticity verification, set **Enable SSL Verification** to “Yes.”

   - To require that customers enter a CVV code, set **Require CVV Entry** to “Yes.”

     ![Advanced Settings]({% link images/images/config-sales-payment-methods-paypal-payflow-pro-advanced-settings.png %}){: .zoom}
     _Advanced Settings_

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline}the **CVV and AVS Settings** section.

1. To determine when a transaction should be rejected when the Address Verification System identifies a mismatch, specify how to handle each of the following scenarios:

   - To reject a transaction based on a mismatched street mismatch, set **AVS Street Does Not Match** to “Yes.”

   - To reject a transaction based on a mismatched ZIP code, set **AVS Zip Does Not Match** to “Yes.”

   - To reject a transaction based on mismatched country identifier, set **International AVS Indicator Does Not Match** to “Yes.”

   - To reject a transaction based on a mismatched CVV code, set **Card Security Code Does Not Match** to “Yes.”

     ![CVV and AVS Settings]({% link images/images/config-sales-payment-methods-paypal-payflow-pro-advanced-settings-cvv-avs.png %}){: .zoom}
     _CVV and AVS Settings_

1. Complete the following, as needed for your store:

#### Settlement Report Settings

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline}the **Settlement Report Settings** section.

1. If you have signed up for PayPal’s Secure FTP Server, enter the following SFTP login credentials:

   - Login
   - Password

1. To run test reports before “going live” with Express Checkout on your site, set **Sandbox Mode** to “Yes.”

1. Enter the **Custom Endpoint Hostname or IP Address**. By default, the value is: reports.paypal.com

1. Enter the **Custom Path** where reports are saved. By default, the value is: /ppreports/outgoing

1. To generate reports according to a schedule, under Scheduled Fetching, make the following settings:

   - Set **Enable Automatic Fetching** to “Yes.”

   - Set **Schedule** to one of the following:

     - Daily
     - Every 3 Days
     - Every 7 Days
     - Every 10 Days
     - Every 14 Days
     - Every 30 Days
     - Every 40 Days

     PayPal retains each report for forty-five days.

   - Set **Time of Day** to the hour, minute, and second when you want the reports to be generated.

     ![PayPal Settlement Report Settings]({% link images/images/config-sales-payment-methods-paypal-payments-advanced-settlement-report-settings.png %}){: .zoom}
     _PayPal Settlement Report Settings_

#### Frontend Experience Settings

The frontend experience settings give you the opportunity to choose which PayPal logos appear on your site, and to customize the appearance of your PayPal merchant pages.

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline}the **Frontend Experience Settings** section.

1. Choose the **PayPal Product Logo** that you want to appear in the PayPal block in your store. The PayPal logos are available in four styles and two sizes. Options include:

   - No Logo
   - We Prefer PayPal (150 x 60 or 150 x 40)
   - Now Accepting PayPal (150 x 60 or 150 x 40)
   - Payments by PayPal (150 x 60 or 150 x 40)
   - Shop Now Using (150 x 60 or 150 x 40)

1. To customize the appearance of your PayPal merchant pages, do the following:

   - Enter the name of the **Page Style** that you want to apply to your PayPal merchant pages. Options include:

     |**paypal** |Uses the PayPal page style.|
     |**primary** |Uses the page style that you identified as the “primary” style in your account profile.|
     |**your_custom_value** |Uses a custom payment page style, which is specified in your account profile.|

   - In the **Header Image URL** field, enter the URL of the image that you want to appear in the upper-left corner of the payment page. The maximum file size is 750 pixels wide by 90 pixels high.

     {:.bs-callout .bs-callout-info}
     PayPal recommends that the image be located on a secure (https) server. Otherwise, the customer’s browser may warn that “the page contains both secure and nonsecure items.”

   - Enter the six-character hexadecimal code, without the “#” symbol, for each of the following:

     |**Header Background Color** |Background color for the checkout page header.|
     |**Header Border Color** |2-pixel border around the header. |
     |**Page Background Color** |Background color for the checkout page and around the header and payment form.|

     ![PayPal Frontend Experience Settings]({% link images/images/config-sales-payment-methods-paypal-payments-advanced-frontend-experience-settings.png %}){: .zoom}
     _PayPal Frontend Experience Settings_

### Step 6: Basic Settings - PayPal Express Checkout

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline}the **Basic Settings - PayPal Express Checkout** section.

1. Enter a **Title** to identify this payment method during checkout. It is recommended to set the title to “PayPal” for each store view.

1. If you offer multiple payment methods, enter a number in the **Sort Order** field to determine the sequence in which PayPal Payments Standard is listed with the other methods. Payment methods appear in ascending order based on the Sort Order value.

1. Set **Payment Action** to one of the following:

   |**Authorization** |Approves the purchase and puts a hold on the funds. The amount is not withdrawn until it is “captured” by the merchant.|
   |**Sale** |The amount of the purchase is authorized and immediately withdrawn from the customer’s account.|

1. To display the “Check out with PayPal” button on the product page, set **Display on Product Details Page** to “Yes.”

   ![Express Checkout Basic Settings]({% link images/images/config-sales-payment-methods-paypal-payments-pro-express-checkout-basic-settings.png %}){: .zoom}
   _Express Checkout Basic Settings_

### **Step 7:** Advanced Settings - PayPal Express Checkout

1. Click to expand the **Advanced Settings** section. Then, do the following:

   - Set **Display on Shopping Cart** to “Yes.”

   - Set **Payment Applicable From** to one of the following:

     |**All Allowed Countries** |Customers from all [countries]({% link stores/country-options.md %}) specified in your store configuration can use this payment method. |
     |**Specific Countries** |After choosing this option, the Payment from Specific Countries list appears. Hold down the Ctrl key and select each country in the list where customers can make purchases from your store. |


   * Set **Debug Mode** to “Yes” to write communications with the payment system into the log file.

     {:.bs-callout .bs-callout-info}
     In accordance with PCI Data Security Standards, credit card information is not recorded in the log file.

   - To enable host authenticity verification, set **Enable SSL Verification** to “Yes.”

   - To display a full summary of the customer’s order by line item from the PayPal site, set **Transfer Cart Line Items** to “Yes.”

   - To allow the customer to complete the transaction from the PayPal site without returning to your Magento store for Order Review, set **Skip Order Review Step** to “Yes.”

     ![Express Checkout Advanced Setting]({% link images/images/config-sales-payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png %}){: .zoom}
     _Express Checkout Advanced Settings_

1. When complete, tap <span class="btn">Save Config</span>.

### **Step 8:** Add Google reCAPTCHA 

To better protect PayPal PayFlow Pro checkout, enable Google reCAPTCHA. It includes options to run reCAPTCHA using a clickable interface or an invisible check to validate the customer. We recommend the invisible option to increase sales conversion and protect your store. For details, see [Google reCAPTCHA]({% link stores/security-google-recaptcha.md %}).

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_US/vhelp/paypalmanager_help/credit_card_numbers.htm
