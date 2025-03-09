# Notion

Notion is a versatile workspace application that combines note-taking, project management, databases, wikis, and more. It allows users to create and organize information in a highly customizable way.&#x20;

Uniquery simplifies the process of accessing and analyzing your Notion data directly within Google Sheets. Instead of manually copying and pasting data, Uniquery establishes a secure connection to the Notion API using OAuth 2.0 authentication.&#x20;

### **Notion Actions in Uniquery**

Uniquery interacts with Notion through a set of _`actions`_. These actions determine what type of data you retrieve and how you interact with the Notion API. Uniquery supports the following actions:

* **Import a database (`getDatabase`):** Retrieves the complete contents of a specified Notion database, including all properties and rows. This is the simplest way to get all data from a database.
* **Query a database (`queryDatabase`):** Retrieves data from a Notion database based on a specific query, filter, and sort criteria that you define using JSON. This provides fine-grained control over the data you import.
* **List all databases (`listDatabases`):** Retrieves a list of all databases shared with the Uniquery integration. This is useful for discovering database IDs for use with other actions. This doesn't import database _content_; it only lists the databases themselves.
* **Search (`search`):** Performs a search across your Notion workspace, similar to Notion's built-in search. You can use a JSON query to specify search terms and filters.

### **Choosing a Database (for `getDatabase` and `queryDatabase`)**

When using the `Import a database` or `Query a database` actions, you'll need to select the specific Notion database you want to work with. Uniquery provides a convenient way to do this:

1. **Connect to Notion:** In the Uniquery sidebar, go to "Manage Connections" and add a connection to your Notion workspace.
2. **Refresh Databases:** In the "Create Report" section for Notion, click the "Refresh databases" button. This will fetch a list of all databases shared with the Uniquery integration.
3. **Select Database:** Choose the desired database from the "Choose database" dropdown menu. This dropdown will populate after you refresh the database list. The dropdown displays database names, the value are database Ids.

### **Using Query JSON (for `queryDatabase` and `search`)**

The `Query a database` and `Search` actions allow you to use Notion's powerful query language to specify which data you want to retrieve. This is done using a JSON (JavaScript Object Notation) object.

*   **Query JSON (for `queryDatabase`):** Enter a valid JSON object in the "Query JSON" text area to filter, sort, and otherwise refine the data retrieved from the selected database. Refer to the [Notion API documentation](https://developers.notion.com/reference/post-database-query) for details on the query syntax.

    *   **Example (Filter):**

        JSON

        ```json
        {
          "filter": {
            "property": "Status",
            "select": {
              "equals": "Done"
            }
          }
        }
        ```

        This example filters the database to only include rows where the "Status" property (which is assumed to be a "select" property) is equal to "Done".
    *   **Example (Sort):**

        JSON

        ```json
        {
          "sorts": [
            {
              "property": "Due Date",
              "direction": "ascending"
            }
          ]
        }
        ```

    This example sorts the database by the "Due Date" property in ascending order.
*   **Query JSON (for `search`):** Enter a valid JSON object to define your search criteria. Refer to the [Notion API documentation](https://developers.notion.com/reference/post-search) for the search query syntax.

    *   **Example:**&#x4A;SON

        ```json
        {
            "query": "Project A",
              "filter": {
                "value": "page",
                "property": "object"
            }
        }
        ```

    This will search "Project A" and only return pages.

### **Example: Importing a Notion Database**

1. **Connect to Notion:** Go to "Manage Connections" and connect your Notion workspace.
2. **Create a Report:** Go to "Create report."
3. **Select Action:** Choose "Import a database" from the "Choose an action" dropdown.
4. **Refresh Databases:** Click "Refresh databases."
5. **Choose Database:** Select the database you want to import from the "Choose database" dropdown.
6. **Generate Report:** Click the button to generate the report. Uniquery will import the entire database into your Google Sheets, with each property becoming a separate column.

### **Example: Querying a Notion Database**

1. **Connect to Notion:** Go to "Manage Connections" and connect your Notion workspace.
2. **Create a Report:** Click on the "Create" button.
3. **Select Action:** Choose "Query a database" from the "Choose an action" dropdown.
4. **Refresh Databases:** Click "Refresh databases."
5. **Choose Database:** Select the database you want to query from the "Choose database" dropdown.
6. **Enter Query JSON:** In the "Query JSON" text area, enter a valid JSON object to define your filter and sort criteria.
7. **Generate Report:** Click the button to generate the report. Uniquery will import the filtered and sorted data into your Google Sheet.

By using the different actions and query capabilities, you can create a wide range of reports in Google Sheets to analyze your Notion data, track progress, and integrate it with other information.
