# Connect to Notion

Integrating Notion with Google Sheets is a powerful way to automate and streamline your workflow, saving you time and effort. Uniquery, a versatile Google Sheets API connector, facilitates this integration by allowing you to create API queries with OAuth2 connections easily. This guide will walk you through the steps of connecting your Google Sheets to your Notion workspace via Uniquery.

### Step 1: Open the Uniquery Add-on

1. Open your Google Sheets document.
2. Go to the **Extensions** menu at the top toolbar.
3. Find **Uniquery** in the dropdown list and click to open the add-on panel within Google Sheets.

### Step 2: Create an OAuth2 Connection

1. Within the Uniquery panel, locate and open the menu to **Create “OAuth2 connection”**.

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* This option is designed to securely manage the authentication required to connect with external services like Notion.

### Step 3: Connect to Notion

1. In the list of available OAuth2 connections, expand the **Notion** option.
2. Click on **“Add connection”**. This action prompts Notion’s authorization process to start.

### Step 4: Authorize Uniquery in Notion

1. A pop-up window will appear, initiating the authorization process for your Notion workspace.
2. Log in to your Notion account if not already logged in.
3. **Choose the pages and databases** you wish to allow Uniquery access to. It’s important to select only the databases you plan to interact with through your Google Sheets.
4. Confirm your selections and grant the necessary permissions.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

### Step 5: Finalize the Connection

1. After successfully authorizing Uniquery, the pop-up will close, and your Notion workspace should now be listed under your **OAuth2 connections** in the Uniquery panel.

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

1. You’ve now successfully established a link between your Google Sheets and Notion workspace.

### Step 6: Use the Authorization in API Queries

1. With the Notion workspace connected, you can proceed to create API queries that interact with your Notion data.
2. Go to the **Create query** editor page within the Uniquery panel.
3. Here, you’ll have the option to select your newly-established Notion OAuth2 connection for your queries.
4. Upon selection, Uniquery will automatically handle the OAuth2 authorization headers, streamlining the process of querying your Notion data.

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

By following these steps, you can now seamlessly integrate and manipulate your Notion databases from within Google Sheets using Uniquery. This connection not only optimizes your productivity but also opens a myriad of possibilities for managing and analyzing your Notion data more efficiently.

Remember, with great power comes the responsibility to manage your connections and data securely. Always ensure that you authorize only the necessary access and keep your OAuth2 connections updated.
