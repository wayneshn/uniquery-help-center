# Airtable

Airtable is a cloud-based, collaborative platform that combines the features of a spreadsheet and a database. It allows users to create flexible, relational databases to organize and manage data, track projects, and build custom workflows.

Uniquery streamlines accessing and analyzing your Airtable data directly within Google Sheets. Instead of manually exporting CSV files from Airtable, Uniquery establishes a secure, direct connection to the Airtable API using OAuth 2.0 authentication.&#x20;

### **Airtable Actions in Uniquery**

Uniquery interacts with Airtable through a set of _actions_. These actions determine what type of data you retrieve. Uniquery supports the following actions:

* **Imports a table (`getTableRecords`):** Retrieves all records (rows) from a specified Airtable table, including all fields (columns). This is the primary action for getting your Airtable data into Google Sheets.
* **List all bases (`listBases`):** Retrieves a list of all Airtable bases that the Uniquery integration has access to. This action is useful for discovering base IDs and understanding which bases are available. This action _does not_ import the data within the bases; it only lists the bases themselves.

### **Specifying the Table URL (for `getTableRecords`)**

When using the `Imports a table` action, you'll need to provide the URL of the specific Airtable table you want to import. Here's how to find the table URL:

1. **Open your Airtable base and table:** Navigate to the specific table you want to import within your Airtable base.
2. **Copy the URL from your browser's address bar:** The URL should look something like this: `https://airtable.com/appXXXXXXXXXXXXXX/tblYYYYYYYYYYYYYY/viwZZZZZZZZZZZZZZ`
   * `appXXXXXXXXXXXXXX` is the Base ID.
   * `tblYYYYYYYYYYYYYY` is the Table ID.
   * `viwZZZZZZZZZZZZZZ` is the View ID.
   * The URL can also contain block information.
3. **Paste the URL into Uiquery** Paste this full URL into the "Table URL" field in the Uniquery sidebar.

### **Example: Importing an Airtable Table**

1. **Connect to Airtable:** In the Uniquery sidebar, go to "Manage Connections" and add a connection to your Airtable account.
2. **Create a Report:** Click on "Create" button.
3. **Select Action:** Choose "Imports a table" from the "Choose an action" dropdown.
4. **Enter Table URL:** Paste the URL of your Airtable table into the "Table URL" field.
5. **Generate Report:** Click the button to generate the report. Uniquery will import all records from the specified table into your Google Sheet. Each field in your Airtable table will become a separate column in the spreadsheet.

### **Example: Listing All Bases**

1. **Connect to Airtable:** In the Uniquery sidebar, go to "Manage Connections" and add a connection to your Airtable account.
2. **Create a Report:** Go to "Create report".
3. **Select Action:** Choose "List all bases" from the "Choose an action" dropdown.
4. **Generate Report:** Click the button to generate the report. Uniquery will import a list of your Airtable bases (including base IDs and names) into your Google Sheet. This is useful for reference, especially if you need to find the base ID for other integrations or API calls.

By using these actions, you can efficiently retrieve data from your Airtable bases and tables, bringing it into Google Sheets for further analysis, reporting, and integration with other data sources.&#x20;
