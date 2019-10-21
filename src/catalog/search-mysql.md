---
title: MySQL
group: marketing
---

MySQL is the default search engine. By adjusting the Catalog Search configuration, you can control the behavior of the search operations and determine the size of valid query text and the display of search recommendations. By default, MySQL always has the EAV Indexer enabled. This feature improves indexation speed and restricts the indexer from use by 3rd party extensions.

![]({% link images/images/config-catalog-catalog-search-mysql.png %}){: .zoom}
*[MySQL Configuration]({% link configuration/catalog/catalog.md %})*

## To configure MySQL search

1. On the Admin sidebar, tap **Stores**. Then under **Settings**, choose **Configuration**.

1. In the panel on the left under **Catalog**, choose **Catalog**.

1. Expand ![]({% link images/images/btn-expand.png %}) the **Catalog Search** section.

1. By default, the **Search Engine** is set to “MySQL”. If switching to MySQL, select that option. This affects the available fields.

1. To limit the length and word count of search query text, set the **Minimal Query Length** and **Maximum Query Length**.

    {: .bs-callout .bs-callout-info}
    **Important:** The value set for this minimum and maximum range must be compatible with the corresponding range set in your MySQL search engine configurations. For example, if you set these values to 2 and 300 in Magento, update the values in your search engine.

1. To limit the amount of popular search results to cache for faster responses, set an amount for **Number of top search results to cache**.

    The default is 100. Entering a value of 0 caches all search terms and results when entered a second time.

1. To limit the maximum number of search results to display for search autocomplete, set an amount for **Autocomplete Limit**. Restricting this amount increases performance of searches and reduces the displayed list size. The default amount is 8.

1. To display search suggestions, set **Enable Search Suggestions** to “Yes”. Additional configuration options display.

    * In the **Search Suggestion Count** field, enter the number of suggestions to offer for each search term that returns no results.  The default is 2.

    * To display the number of search results for each suggested term, set **Show Results Count for Each Suggestion** to “Yes”.

1. To offer search recommendations, set **Enable Search Recommendations** to “Yes.” Additional configuration options display.

    * In the **Search Recommendations Count** field, enter the number of recommendations that you want to offer. The default is 5.

    * To display the number of results for each recommendation, set **Show Results Count for Each Recommendation** to “ Yes”.

1. When complete, tap <span class="btn"> Save Config </span>.
