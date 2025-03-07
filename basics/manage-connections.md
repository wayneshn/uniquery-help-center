# Manage connections

The Manage Connections feature is crucial for creating connections between Google Sheets and external APIs using Uniquery. It supports custom OAuth 2.0 flows, enabling users to connect with platforms not available in Uniquery's preset integrations.

Here are some of the preset integrations we support:

* Facebook Ads&#x20;
* Google Ads&#x20;
* Google Analytics&#x20;
* Linkedin Ads&#x20;
* Hubspot&#x20;
* Mailchimp&#x20;
* Stripe&#x20;
* Google Search Console&#x20;
* Google My Business&#x20;
* Shopify&#x20;
* Zendesk&#x20;
* MySQL&#x20;
* PostgreSQL

This list is continuously growing as we add more integrations to Uniquery.

## &#x20;Manage Connections in Google Sheets Addon

To manage connections in the Uniquery addon, start by opening a new or existing Google Sheets file. Navigate to the menu bar and click on `Extensions`. From the dropdown menu, select `Uniquery` to open the addon.&#x20;

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

In the Uniquery sidebar, locate the `Create` button. Click on the `Create` button and select `Manage Connections` from the dropdown menu. A new window will appear displaying a list of all available integrations that you can connect to.

### Connect to a Data Source

To connect to a data source, first, select an integration from the list of available integrations. For example, if you want to connect to Google Analytics, click on the `Add Connection` button next to the Google Analytics integration.&#x20;

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

An authorization page will appear where you need to authorize your account. Follow the prompts to log in to your account and ensure that you grant Uniquery all requested permissions to successfully pull your data. Once the authorization process is complete, you will be redirected back to Google Sheets, and the new connection will now appear in your list of managed connections.

### Use Connections in Queries

You can use your connected data sources in the `Create report` or `API query` sections of Uniquery.&#x20;

To use a connection in the `Create report` page, navigate to the Uniquery sidebar and select the `Create report` option. Based on the report you are creating, choose the corresponding connection.&#x20;

For example, if you are creating a Facebook Ads report, select the Facebook Ads connection you have already established, and follow the prompts to generate your report using the selected connection.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

To use a connection in the `API query` section, navigate to the Uniquery sidebar and select the `API query` option.&#x20;

Use the dropdown menu to select the connection you want to use for your API query. Ensure that your API query is authenticated using the selected connection by following the prompts to complete the query setup. Once the setup is complete, execute the API query to retrieve data from the connected data source.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

