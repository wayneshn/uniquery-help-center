---
description: >-
  Uniquery is a Google Sheets addon that connects Google Sheets with external
  data sources. By importing data directly into Sheets, it streamlines data
  management and analysis. The addon can be installe
---

# How Uniquery works?

Uniquery currently is a Google Sheets addon designed to facilitate the connection between Google Sheets and various external data sources. By using Uniquery, users can import data from these sources directly into their Google Sheets, enabling efficient data management and analysis.

### Installation

To use Uniquery, you first need to install the addon from the Google Workspace Marketplace. Follow these steps:

1. Open Google Sheets.
2. Navigate to `Extensions` in the menu bar.
3. Select `Add-ons` and then `Get add-ons`.
4. In the Google Workspace Marketplace, search for "Uniquery". Or use this [direct install link](https://workspace.google.com/marketplace/app/uniquery_api_connector_with_oauth_2_supp/275511172491).
5. Click on the Uniquery addon and select `Install`.

Once installed, the Uniquery addon will be available under the `Extensions` menu in Google Sheets.

### Connecting to Data Sources

Uniquery allows users to connect to a variety of external data sources. These connections can be managed through the Manage Connections feature. Here is how you can connect to a data source:

1. Open Google Sheets and navigate to `Extensions > Uniquery` to open the addon.
2. In the Uniquery sidebar, click on the `Create` button and select `Manage Connections`.
3. A new window will display a list of available integrations.
4. Select the desired integration and click on the `Add Connection` button.
5. An authorization page will appear. Follow the prompts to log in and authorize your account.
6. Once authorization is complete, the connection will be added to your list of managed connections.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

### Creating Reports

Uniquery provides functionality for generating reports based on the connected data sources. To create a report, follow these steps:

1. In the Uniquery sidebar, navigate to the `Create report` page.
2. Select the type of report you wish to create from the available options.
3. Choose the corresponding connection that you have already established.
4. Follow the prompts to configure the report parameters, adding metrics and dimensions, or date range.
5. Generate the report, and the data will be imported into your Google Sheets.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

### Executing API Queries

In addition to generating reports, Uniquery allows users to execute general API queries. This feature is useful for custom data retrieval tasks. To execute an API query:

1. In the Uniquery sidebar, navigate to the `API query` page.
2. Select the connection you want to use for the API query from the dropdown menu.
3. Provide the necessary query parameters and configuration, such as headers, and request body.
4. Your API query can be authenticated using the selected connection (OAuth 2).
5. Execute the query to retrieve data from the connected data source.

When dealing with large datasets, pagination is often required to retrieve all data. Uniquery provides built-in support for handling pagination in API queries. To handle pagination:

1. In the `API query` page, configure your query parameters as usual.
2. Specify the pagination parameters, such as the page number and page size, according to the API documentation of the data source.
3. Uniquery will automatically handle the pagination by retrieving data in multiple requests and combining the results.
4. Execute the query to retrieve the complete dataset.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

This feature simplifies the process of working with large datasets by ensuring that all data is retrieved and combined seamlessly.

### Automated Data Refresh

Uniquery supports automated data refresh to ensure that your data remains up-to-date. This feature allows users to schedule data refresh for created reports and API queries at specified intervals, such as hourly, daily, or weekly. To set up automated data refresh:

In the Uniquery sidebar, navigate to the `In this spreadsheet` page. Select the query for which you want to enable automated data refresh. Configure the refresh interval and other relevant settings. Save the configuration. Uniquery will automatically refresh the data at the specified intervals.

### Conclusion

Uniquery is a powerful tool for integrating Google Sheets with various external data sources. By following the steps outlined in this documentation, users can efficiently connect, manage, and utilize data from multiple platforms within their Google Sheets environment.
