# Shopify

Shopify is a leading e-commerce platform that allows businesses to create and manage online stores. It provides a comprehensive suite of tools for handling everything from product listings and inventory management to order processing, payments, and shipping.&#x20;

Shopify's robust reporting features offer insights into sales, customer behavior, and overall store performance. However, for advanced analysis and reporting, integrating Shopify data with other data sources is often necessary.

Okay, here's a revised draft for the Shopify data source section, reflecting Uniquery's approach of retrieving "resources" rather than explicitly defining metrics and dimensions:

### **Shopify Resources in Uniquery**

Instead of using the traditional "metrics" and "dimensions" terminology, Uniquery works with Shopify _resources_. A resource represents a type of data object within Shopify, such as an Order, a Product, or a Customer. Each resource has a set of associated _fields_ that contain the specific data points. When you create a Shopify report in Uniquery, you select the resource you want to import.

### **Shopify Resources Supported by Uniquery**

Uniquery supports importing data from the following Shopify resources:

* **Orders:** Contains all information related to orders placed in your store, including order details, line items, customer information, shipping and billing addresses, payment details, refunds, and fulfillment status.
* **Products:** Contains information about your products, including titles, descriptions, variants (with prices and SKUs), inventory levels (through associated Inventory Level objects), images, and more.
* **Collects:** Represents the relationships between products and collections. Useful for understanding which products belong to which collections.
* **Events:** Records various events that occur within your Shopify store, such as order creation, product updates, and customer account changes.
* **Gift cards:** Contains data on gift cards issued by your store.
* **Custom collections:** Contains information of your custom collections.
* **Marketing events:** Contains marketing activities.
* **Blogs** Contains blog posts

### **Filtering Shopify Data (Order Status)**

For the `Orders` resource, Uniquery provides an additional filtering option:

* **Order Status:** You can choose to import orders with a specific status:
  * **Any:** Imports all orders, regardless of status.
  * **Open:** Imports only orders that are currently open (not yet fulfilled or canceled).
  * **Closed:** Imports only orders that have been fulfilled.
  * **Canceled:** Imports only orders that have been canceled.

This allows you to focus your reports on specific subsets of your order data.

### **Limiting the Number of Records (Limit)**

The Shopify API has limits on the number of records that can be retrieved in a single request. Uniquery allows you to specify a `Limit` for your data import:

* **Limit (Optional):** Enter the number of records you want to import. The default value is 50. The maximum value is 250, due to Shopify's API limitations. Uniquery automatically handles pagination, so even if you set a limit of 250, and there are more than 250 records, running the query again will retrieve the next set of records.

### **Example: Importing Order Data**

To import order data into your Google Sheet:

1. **Connect to Shopify:** In the Uniquery sidebar, go to "Manage Connections" and add a connection to your Shopify store.
2. **Create a Report:** Go to the "Create Report" page.
3. **Select Resource:** Choose "Orders" from the "Choose a Shopify resource type to import" dropdown.
4. **Filter by Status (Optional):** Select the desired "Order status" (Any, Open, Closed, or Canceled).
5. **Set Limit (Optional):** Enter a value for "Limit" (maximum 250). Leave blank for the default of 50.
6. **Generate Report:** Click the button to generate the report. Uniquery will import the specified order data into your Google Sheet. The data will be presented with each field (e.g., `order_number`, `created_at`, `total_price`, `customer.email`, etc.) as a separate column.

**Example: Importing product data** To import product data, select "Products" as resource, set limits, and then click the button to generate the report. All product data will be imported into the Google Sheet.

By selecting different resources and using the available filtering and limiting options, you can create a wide variety of reports in Google Sheets to analyze your Shopify data and gain valuable insights into your store's performance.
