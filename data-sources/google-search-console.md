# Google Search Console

Google Search Console is a free service offered by Google that helps you monitor, maintain, and troubleshoot your site's presence in Google Search results. It provides valuable insights into how Google sees your website, including: &#x20;

* **Search Performance:** See which queries bring users to your site, how often your site appears in search results (impressions), how often users click on your site (clicks), your average position in search results, and your click-through rate (CTR).
* **Indexing Status:** Understand how Google is crawling and indexing your website, identify any indexing errors, and submit sitemaps to help Google discover your content.
* **Mobile Usability:** Check for mobile-friendliness issues that could affect your site's ranking in mobile search results.
* **Security Issues:** Receive alerts about any security problems detected on your site, such as malware or hacking.
* **Links to Your Site:** See which websites are linking to your site (backlinks), which is a crucial factor in search engine ranking.

Effectively using Google Search Console data is essential for improving your website's organic search visibility and driving more traffic from Google.

### **How a Google Search Console Connection Works in Uniquery**

Uniquery simplifies the process of retrieving and analyzing your Google Search Console data directly within Google Sheets. Instead of manually downloading CSV reports from the Search Console interface, Uniquery establishes a secure, direct connection to the Google Search Console API using OAuth 2.0 authentication. This connection allows you to:

* **Automate Data Retrieval:** Pull your Search Console performance data directly into your spreadsheets.
* **Customize Reports:** Select specific metrics and dimensions to build reports tailored to your SEO analysis needs.
* **Schedule Refreshes:** Keep your data up-to-date with automatic hourly, daily, or weekly refreshes.
* **Combine Data Sources:** Integrate Search Console data with data from other platforms (like Google Analytics, LinkedIn Ads, etc.) for a complete picture of your online performance.
* Directly access the Google Search Console API and extract the response to Google Sheets.

### **Metrics**

In Google Search Console, _metrics_ represent the quantitative measurements of your website's performance in Google Search. They provide the numerical data that shows how your site is performing.&#x20;

Okay, here's the table for Google Search Console _metrics_ supported by Uniquery, including Tag, Name, and a Description:

| Tab           | Name                     | Description                                                                                                                                                         |
| ------------- | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `clicks`      | Clicks                   | The number of times users clicked on your website's listing in Google Search results. A direct measure of how much traffic Google Search is sending to your site.   |
| `impressions` | Impressions              | The number of times your website's listing appeared in Google Search results. Indicates how often your site is being seen by users.                                 |
| `ctr`         | CTR (Click-Through Rate) | The percentage of impressions that resulted in a click (Clicks / Impressions). A higher CTR indicates that your search result listings are compelling and relevant. |
| `position`    | Average Position         | The average position of your website's listing in search results for a given query or page. Lower numbers are better (position 1 is the top result).                |

### **Dimensions**

_Dimensions_ in Google Search Console provide context to your metrics. They allow you to segment your data and analyze performance across different categories. Dimensions are attributes that describe your data, enabling you to break down your metrics.

| Tag                | Name              | Description                                                                                                                                                                                  |
| ------------------ | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `query`            | Search query      | The actual search terms users typed into Google to find your site. Essential for understanding what keywords are driving traffic and identifying new keyword opportunities.                  |
| `country`          | Country           | The country where the user was located when they performed the search. Useful for understanding your geographic reach and tailoring content to specific regions.                             |
| `device`           | Device            | The type of device used to perform the search (e.g., "desktop," "mobile," "tablet"). Important for optimizing your site for different device types and understanding user behavior on each.  |
| `page`             | Page              | The specific page on your website that appeared in the search results. Allows you to analyze the performance of individual pages and identify which pages are ranking well.                  |
| `searchAppearance` | Search appearance | How your search result listing appeared in Google Search. Examples include "AMP article," "Rich result," "Video," "Web Light result," etc. Helps you understand the impact of rich snippets. |
| `date`             | Date              | Segments your data.                                                                                                                                                                          |

