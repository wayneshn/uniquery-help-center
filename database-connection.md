# Database connection

The Database Connection feature in Uniquery allows you to seamlessly connect Google Sheets with various SQL databases, including MySQL, Microsoft SQL Server, and PostgreSQL. This integration enables you to manage and analyze your data directly within Google Sheets, enhancing your productivity and data handling capabilities.

### Open the Uniquery Addon

To begin, open a new or existing Google Sheets file. Once you have your spreadsheet open, navigate to the menu bar at the top of the page. Click on the `Extensions` menu item to reveal a dropdown menu. From this dropdown, select `Uniquery` to open the addon. This action will display the Uniquery sidebar, where you can manage your connections and create reports.

### Add a Database Connection

In the Uniquery sidebar, locate the `Create` button. Click on this button to reveal a dropdown menu. From the dropdown, select `Manage Connections`. A new window will appear, displaying a list of all available integrations you can connect to. To add a new database connection, click on the any database connection, such as PostgreSQL.

### Select Database Type

In the new window, you will be prompted to select the type of database you want to connect to. Uniquery supports several database types, including MySQL, Microsoft SQL Server, and PostgreSQL. Choose the appropriate database type from the available options by clicking on it.

### Enter Database Details

After selecting the database type, you will need to enter the necessary details to establish the connection. Fill in the following fields with your database information:

* **Database host**: Enter the host name of your database. This can be a domain name (e.g., your\_database\_host.com) or an IP address. Ensure that you do not include `http://`, `https://`, or the port number in this field.
* **Database port**: Enter the port number of your database. The port number varies depending on the database type. For example, the default port number for MySQL is `3306`, while PostgreSQL typically uses `5432`. If you are unsure of the port number, check your database setup.
* **Database name**: Enter the name of your database.
* **User name**: Enter the username you use to access your database.
* **Password**: Enter the password associated with your database username.

### Whitelist IP Addresses (if necessary)

Depending on the database type you selected, you may need to whitelist certain IP addresses to allow access to your database. This step is crucial if your database is protected by a firewall.

* For MySQL and Microsoft SQL Server, the database connector relies on Google's JDBC service. You will need to whitelist the IP addresses provided by Google. You can find the list of IP addresses [here](https://www.gstatic.com/ipranges/goog.txt).
* For PostgreSQL, the database connector relies on Uniquery's proxy servers. You will need to whitelist the following IP address: `18.199.186.79`.

### Test the Connection

Before finalizing the connection, it is important to test it to ensure that the details you entered are correct. Click the `Test connection` button to initiate the test. Uniquery will attempt to connect to your database using the provided information.

If the connection test is successful, you will see a confirmation message indicating that the connection test succeeded. This means that Uniquery was able to establish a connection to your database with the provided details.

If the connection test fails, an error message will appear. The error message will provide information about why the test failed. Common issues include incorrect host names, port numbers, usernames, or passwords. Double-check your connection configuration and make any necessary corrections before testing the connection again.

### Create the Connection

Once the connection test is successful, you can proceed to create the connection. Click the `Create connection` button to store your database connection in Uniquery. A confirmation message will appear, indicating that the database connection was created successfully.

Your new database connection will now be listed in the `Manage Connections` window. You can use this connection to create reports and run queries within Google Sheets.



\
