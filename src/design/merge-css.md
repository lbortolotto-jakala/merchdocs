---
title: Merging CSS Files
---

As part of an effort to optimize your site and reduce page load time, you can reduce the number of separate CSS files by merging them into a single condensed file. If you open a merged CSS file, you’ll find one continuous stream of text, with line breaks removed. Because you can’t edit the merged file, it’s best to wait until you are out of the development mode, and no longer making frequent changes to the CSS.

{: .bs-callout .bs-callout-info}
CSS files can be merged only when working in [Developer Mode]({% link magento/installation-modes.md %}).

## To merge CSS files:

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the panel on the left under **Advanced**, choose **Developer**.

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline} the **CSS Settings** section.

    ![]({% link images/images/config-advanced-developer-css-settings.png %}){: .zoom}
    [*CSS Settings*]({% link configuration/advanced/developer.md %})

1. Set **Merge CSS Files** to `Yes`.

1. When complete, click <span class="btn">Save Config</span>.
