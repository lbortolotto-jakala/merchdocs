---
title: Using a Content Delivery Network
---

A Content Delivery Network (CDN) can be used to store media files. Although the version of Magento that is installed “on premise” does not include an integration with any specific CDN, you can use the CDN of your choice. [Magento Commerce (Cloud)][1] is an exception to this, and includes the Fastly CDN. See [Fastly][2] in the Magento developer documentation.

After configuring the CDN, you must complete the configuration from the Admin. The changes can be made at either the global or website level. When a CDN is used for media storage, all paths to media on store pages are changed to the CDN paths that are specified in the configuration.

## CDN Workflow

1. **Browser requests media**.—A page from the store opens in the customer’s browser, and the browser requests the media that is specified in the HTML.
1. **Request sent to CDN; images found and served**.—The request is sent first to the CDN. If the CDN has the images in storage, it serves the media files to the customer's browser.
1. **Media not found, request sent to Magento web server**.—If the CDN does not have the media files, the request is sent to the Magento web server. If the media files are found in the file system, the web server sends them to the customer’s browser.

{:.bs-callout-info}
**Important!** 
For security, when a CDN is used as media storage, JavaScript may not function properly if the CDN is located outside of your subdomain.

### To configure a content delivery network

1. On the _Admin_ sidebar, click **Stores**.

1. Under _Settings_, choose **Configuration**.

1. In the panel on the left under _General_, choose **Web**.

1. In the upper-left corner, set **Store View** as needed.

1. Expand ![]({% link images/images/btn-expand.png %}) the **Base URLs** section. Then, do the following:

    ![]({% link images/images/config-general-web-base-urls.png %}){: .zoom}
    [*Base URLs*]({% link configuration/general/web.md %})

    - Update the **Base URL for Static View Files** with the URL of the location on the CDN where static view files are stored.

    - Update the **Base URL for User Media Files** with the URL of the JavaScript files on the CDN.

        Both these fields can be left blank, or can start with the placeholder: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Expand the **Base URLs (Secure)** section.

    ![]({% link images/images/config-general-web-base-urls-secure.png %}){: .zoom}
    [*Base URLs (Secure)*]({% link configuration/general/web.md %})

    - Update the **Secure Base URL for Static View Files** with the URL of the location on the CDN where static view files are stored.

    - Update the **Secure Base URL for User Media Files** with the URL of the JavaScript files on the CDN.

        Both these fields can be left blank, or can start with the placeholder: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. When complete, click **Save Config**.

[1]: https://magento.com/products/magento-commerce
[2]: https://devdocs.magento.com/guides/v2.3/cloud/cdn/cloud-fastly.html
