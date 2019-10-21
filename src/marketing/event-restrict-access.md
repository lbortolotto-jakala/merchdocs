---
conditions: Default.EE-B2B
title: Restricting Access
---

Access to a private sale, event, or site can be limited to registered customers who log in, or extended to non-registered customers who must register before gaining access.

![]({% link images/images-ee/config-general-general-website-restrictions.png %}){: .zoom}
[*Website Restrictions*]({% link configuration/general/general.md -%})

## To set up exclusive access

1. On the Admin sidebar, tap **Stores**. Then under **Settings**, choose **Configuration**.

1. In the panel on the left under **General**, choose **General**.

1. Expand ![]({% link images/images/btn-expand.png %}) the **Website Restrictions** section, and do the following:.

    * Set **Access Restriction** to “Yes".

    * Set **Restriction Mode** to one of the following:

        * Private Sales: Login Only
        * Private Sales: Login and Register

    * Set **Startup Page** to one of the following:

        |--- |--- |
        |To login form (302 Found)|Users are redirected to the login form before gaining access to the site.|
        |To landing page (302 Found)|Users are redirected to the specified landing page until they log in. **Important!** Be sure to include a link to the login page from the landing page so customers can log in to access the site.|
        {:style="table-layout:auto"}

    * Choose the **Landing Page** that appears before customers log in to the private sale site.

    * To let search engine bots and spiders know that the landing page is correct, and that there are no other pages on the site to index. set **HTTP Response** to “200 OK”

    * If you want the fields in the customer login and forgot password forms to be filled automatically from previous entries, set **Enable Autocomplete on login/forgot password forms** to “Yes”.

1. When complete, tap <span class="btn">Save Config</span>.
