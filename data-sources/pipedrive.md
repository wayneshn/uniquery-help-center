# Pipedrive

Pipedrive is a sales-focused CRM (Customer Relationship Management) platform designed to help sales teams manage leads, track deals, and automate their sales processes. It provides a visual pipeline view of deals, allowing for easy tracking of progress through different stages.&#x20;

Uniquery simplifies accessing and analyzing your Pipedrive data directly within Google Sheets. Instead of manually exporting CSV files from Pipedrive, Uniquery establishes a secure, direct connection to the Pipedrive API using OAuth 2.0 authentication.&#x20;

### **Pipedrive Resources in Uniquery**

Uniquery interacts with Pipedrive by retrieving data from different _resources_. A resource represents a type of data object within Pipedrive. Uniquery currently supports the following Pipedrive resources:

* **Persons:** Represents individual contacts in Pipedrive. Includes information like name, email, phone number, organization, and custom fields.
* **Leads:** Represents potential deals that are in the early stages of the sales process. Includes information about the lead, associated contact and organization, and lead value.
* **Deals:** Represents deals in progress, including deal value, stage, close date, associated contact and organization, and custom fields.
* **Projects:** If you use Pipedrive's Projects feature, this resource allows you to retrieve data about your projects.
* **Products:** Represents the products or services you sell. Includes information like product name, code, price, and custom fields.
* **Organizations:** Represents companies or organizations associated with your contacts and deals. Includes information like company name, address, and custom fields.
* **Activities:** Represents activities related to your deals and contacts, such as calls, meetings, emails, and tasks.

### **Filtering Data by Owner ID (Persons and Leads)**

For the `Persons` and `Leads` resources, Uniquery offers an optional filter:

* **Owner ID (Optional):** If you provide a user ID in this field, Uniquery will only import Persons or Leads that are _owned_ by that specific Pipedrive user. Leave this field blank to import all Persons or Leads, regardless of owner.

### **Example: Importing All Deals from Pipedrive**

1. **Connect to Pipedrive:** In the Uniquery sidebar, go to "Manage Connections" and add a connection to your Pipedrive account.
2. **Create a Report:** Go to "Create Report".
3. **Select Resource:** Choose "Import all deals" from the "Choose an action" dropdown.
4. **Generate Report:** Click the button to generate the report. Uniquery will import all your Pipedrive deals into your Google Sheet. Each deal property (e.g., `title`, `value`, `stage_id`, `person_id`, `org_id`) will be a separate column.

### **Example: Importing Leads for a Specific Owner**

1. **Connect to Pipedrive:** In the Uniquery sidebar, go to "Manage Connections" and add a connection to your Pipedrive account.
2. **Create a Report:** Go to "Create report".
3. **Select Resource:** Choose "Import all leads" from the "Choose an action" dropdown.
4. **Enter Owner ID:** In the "Owner ID (Optional)" field, enter the Pipedrive user ID of the owner whose leads you want to import. You can typically find a user's ID in the Pipedrive user management settings or through the Pipedrive API.
5. **Generate Report:** Click the button to generate the report. Uniquery will import only the leads owned by the specified user.

By selecting different resources and using the optional owner ID filter, you can build a variety of reports in Google Sheets to analyze your Pipedrive data and gain valuable insights into your sales performance.&#x20;
