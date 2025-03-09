# Hubspot

HubSpot is a comprehensive _CRM (Customer Relationship Management)_ platform that provides tools for marketing, sales, customer service, and content management. It helps businesses attract visitors, convert leads, close deals, and delight customers.&#x20;

HubSpot's built-in reporting offers many insights, but integrating HubSpot data with other data sources and performing custom analyses is often essential for a complete view of business performance.

### **How a HubSpot Connection Works in Uniquery**

Uniquery streamlines accessing and analyzing your HubSpot data directly within Google Sheets. Instead of manually exporting data from HubSpot, Uniquery establishes a secure, direct connection to the HubSpot API using OAuth 2.0 authentication. This connection allows you to:

* **Automate Data Retrieval:** Pull data from various HubSpot objects (like Contacts, Companies, and Deals) directly into your spreadsheets.
* **Customize Data Imports:** Select the specific HubSpot action you want to perform (currently: importing Contacts, Companies, or Deals).
* **Limit the Number of Records:** Control the amount of data imported in a single request.
* **Schedule Refreshes:** Keep your data up-to-date with automatic hourly, daily, or weekly refreshes (available with a paid Uniquery subscription).
* **Combine Data Sources:** Integrate HubSpot data with data from other marketing platforms, analytics tools, and business systems for a holistic view of performance.
* Directly access the Hubspot API and extract the response to Google Sheets.

Uniquery simplifies data extraction, eliminates manual exports, and provides a powerful way to work with your HubSpot data in Google Sheets.

### **HubSpot Actions in Uniquery**

Uniquery interacts with HubSpot by performing specific _actions_. Currently, Uniquery supports the following actions for importing data:

* **Import Contacts:** Retrieves data about your contacts in HubSpot, including properties like name, email, company, lifecycle stage, and any custom properties you've defined.
* **Import Companies:** Retrieves data about companies in HubSpot, including properties like company name, domain, industry, and any custom company properties.
* **Import Deals:** Retrieves data about your deals in HubSpot, including properties like deal name, amount, stage, close date, associated contacts and companies, and any custom deal properties.

Each of these actions retrieves a set of _records_ (individual contacts, companies, or deals) from HubSpot, along with their associated _properties_ (fields).

### **Limiting the Number of Records (Number of Records)**

The HubSpot API has limits on the number of records that can be retrieved in a single request. Uniquery allows you to specify a limit:

* **Number of records (optional):** Enter the number of records you want to import. The default value is 10. If left blank, Uniquery will import 10 records.

### **Example: Importing Contacts from HubSpot**

To import contact data into your Google Sheet:

1. **Connect to HubSpot:** In the Uniquery sidebar, go to "Manage Connections" and add a connection to your HubSpot account.
2. **Create a Report:** Go to "Create Report."
3. **Select Action:** Choose "Import contacts" from the "Choose an action" dropdown.
4. **Set Limit (Optional):** Enter a value for "Number of records (optional)." Leave blank for the default of 10.
5. **Generate Report:** Click the button to generate the report (the exact button text may vary). Uniquery will import the specified contact data into your Google Sheet. The data will be presented with each contact property (e.g., `firstname`, `lastname`, `email`, `company`, `lifecyclestage`) as a separate column.

### **Example: Importing Companies or Deals**&#x20;

Follow similar procedures to import companies and deals, the only difference is to choose different actions.

By selecting different actions and using the limiting option, you can create various reports in Google Sheets to analyze your HubSpot data and gain insights into your marketing, sales, and customer relationships.
