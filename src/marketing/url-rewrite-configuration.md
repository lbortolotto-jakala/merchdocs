---
title: Configuring URL Rewrites
---

URL rewrites make it possible to make existing URLs more “search engine friendly” and also easier for humans to read. Enabling Web Server Apache Rewrites is part of the initial Magento setup. Magento routinely uses URL rewrites to remove the file name `index.php` that normally appears in the URL just after the root folder. When Web Server Rewrites are enabled, the system rewrites each URL to omit `index.php`. The rewrite removes words that convey nothing of value to search engines or customers, and has no impact on performance or site rank.

URL without Web Server Rewrite

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL with Web Server Rewrite

    http://www.yourdomain.com/magento/storeview/url-identifier

## To configure URL rewrites

1. On the Admin sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the page navigation where **General** is expanded, choose **Web**.

1. Expand ![]({% link images/images/btn-expand.png %}) the **Search Engine Optimization** section.

    ![]({% link images/images/config-general-web-search-engine-optimization.png %}){: .zoom}
    [_Search Engine Optimization_]({% link configuration/general/web.md -%})

1. Set **Use Web Server Rewrites** to your preference.

1. When complete, click <span class="btn">Save Config</span>.