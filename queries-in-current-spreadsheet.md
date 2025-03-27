# Queries in current spreadsheet

The "In this spreadsheet" tab in Uniquery allows users to view and manage all queries that run in the current Google Sheets file. This includes both generated reports and API queries. The tab provides detailed information about each query, making it easier to monitor and maintain data connections.

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

### Viewing Queries

To access the "In this spreadsheet" tab:

1. Open your Google Sheets file and navigate to `Extensions > Uniquery` to open the addon.
2. In the Uniquery sidebar, click on the `In this spreadsheet` tab.

### Information Available

In the "In this spreadsheet" tab, you can check the following information for each query:

#### Data sheet&#x20;

The tab displays the specific sheet within the Google Sheets file where each query runs. This helps users identify the location of the data imported by the query.

#### Last Refreshed

For each query, the tab shows the timestamp of the last data refresh. This information is useful for ensuring that the data is up-to-date and determining when the last update occurred.

#### Auth Refresh Setting

The tab provides details about the authentication refresh setting for each query. This setting indicates whether the query is configured to automatically refresh its authentication tokens, ensuring continuous access to the data source.

#### Adding or Removing Auth Refresh

Users can add or remove authentication refresh settings for each query directly from the "In this spreadsheet" tab. This feature allows users to enable or disable automatic authentication refresh based on their requirements.

To add or remove auth refresh for a query:

1. Locate the query in the "In this spreadsheet" tab.
2. Click on the relevant option to add or remove the auth refresh setting.
3. Save the changes to update the configuration.

The "In this spreadsheet" tab in Uniquery provides a comprehensive overview of all queries running in the current Google Sheets file. By offering detailed information about each query, including sheet location, last refreshed timestamp, and authentication refresh settings, users can efficiently monitor and manage their data connections. The ability to add or remove auth refresh settings further enhances the flexibility and control over data import processes within Google Sheets.
