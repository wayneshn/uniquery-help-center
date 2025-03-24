# MySQL

Uniquery allows you to connect to your MySQL databases directly from Google Sheets, enabling seamless data import and analysis. This guide will walk you through the steps to create a MySQL database connection report using the Uniquery addon.

### Navigating to the Database Connection Report Page

To begin, open Google Sheets and navigate to Extensions > Uniquery to open the addon. In the Uniquery sidebar, click on the Create button and select Database Connection. You will be directed to the Database Connection Report page.

### Setting Up Your Report

On the Database Connection Report page, you will find a form to configure your MySQL database connection and report settings.

#### Report Name

Provide a name for your report in the "Report name" field. This helps you identify the report for future reference. For example, you can name it "My MySQL Import".

#### Select OAuth Connection

Choose the OAuth connection for your MySQL database. If you haven't set up a connection yet, follow the prompts to log in and [connect to your MySQL database](database-connection.md).

#### Choose an Action

Select the action you want to perform with your MySQL database. You have two options:

* Pull data from table: This option allows you to import data from a specific table in your MySQL database.
* Run SQL statement (INSERT only): This option allows you to run an SQL statement (INSERT only) on your MySQL database.

#### Configure Table Name or SQL Statement

If you selected "Pull data from table", provide the name of the table you want to import data from in the "Table name" field.\
If you selected "Run SQL statement (INSERT only)", provide the SQL statement you want to execute in the "SQL statement" field. Note that currently only the SELECT query method is supported.

### Need Help?

If you need assistance with your MySQL database connection, click on the "Need Help" link. This will provide you with additional resources and support for connecting to your MySQL database.

### Save and run

Once you have configured all the necessary settings, save your report. Finally, execute the report to import data from your MySQL database into Google Sheets.

By following these steps, you can easily connect to your MySQL database and create customized reports using Uniquery in Google Sheets. This enables you to manage and analyze your data efficiently, leveraging the powerful capabilities of both MySQL and Google Sheets.
