# New API query

Uniquery offers a powerful solution for integrating external data into Google Sheets through its API Connection feature. This tool allows users to connect seamlessly to various API endpoints, enabling automatic data updates and efficient data management. The key aspects of this feature are outlined in detail below.

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### OAuth 2.0 Support and Pagination Handling&#x20;

One of the significant technical features of Uniquery is its support for OAuth 2.0. This protocol is essential for secure and seamless connectivity to various API endpoints, which is particularly crucial for marketers and data analysts who need access to data across multiple platforms. OAuth 2.0 simplifies the authentication process, ensuring that connections are both secure and reliable.

Additionally, Uniquery efficiently handles pagination in APIs. Many APIs limit the amount of data returned in a single request, delivering it in multiple "pages" instead. Uniquery automatically manages these pages, collecting all the necessary data across multiple requests and compiling it into a single, comprehensive dataset. This feature saves users from the manual hassle of pagination and allows them to focus more on data analysis and interpretation.

### Step-by-Step Guide to Using the API Connector

#### **Step 1: Create a New API Query**&#x20;

1. Open Google Sheets and navigate to the Uniquery add-on from the Extensions menu.
2. In the Uniquery sidebar, click on the "Create" button and select "New API query" from the dropdown menu.
3. Enter a name for your query in the "Name" field. This helps you identify the API query in future projects.

#### **Step 2: Configure the HTTP Method and URL**

1. Select the appropriate HTTP method (GET, POST, PUT, DELETE, or PATCH) from the dropdown menu. The method you choose indicates the action you intend to perform, such as retrieving data (GET) or creating new records (POST).
2. Enter the API endpoint URL in the "URL" field. Ensure you use the precise URL as outlined in the API documentation.

\
Example:\
For a dummy JSON endpoint, you can use the following URL:

```javascript
https://jsonplaceholder.typicode.com/posts  
```

#### **Step 3: Add Optional Parameters and Headers**&#x20;

Use the "Parameters" section to specify any criteria or filters for your API request by adding key-value pairs. For example, you can add a parameter to retrieve records from a particular date onwards.

Add headers to your API request in the "Request headers" section. Headers allow you to specify metadata associated with your request, such as the content type or authorization credentials.

Headers provide metadata about your request, such as content type or authorization credentials. Here are some examples of common headers:\


1. **Content Type Header**:
   * **Key**: `Content-Type`
   * **Value**: `application/json`
   * **Description**: This header specifies that the request body is formatted in JSON.\

2. **Authorization Header**:
   * **Key**: `Authorization`
   * **Value**: `Bearer YOUR_ACCESS_TOKEN`
   * **Description**: This header includes the access token required for authenticating the API request.\

3. **Custom Header**:
   * **Key**: `X-Custom-Header`
   * **Value**: `customValue`
   * **Description**: This is an example of a custom header that might be required by some APIs for specific configurations or custom settings.

#### **Step 4: Add an OAuth 2.0 Connection (Optional)**

&#x20;If your API requires OAuth 2.0 authentication, click on the "Add an OAuth2 Connection" button. Follow the prompts to select and authorize the OAuth connection. This step ensures that your API query is authenticated securely.

**See more:** [**Manage connections**](basics/manage-connections.md)

#### **Step 5: Configure the Request Body (for POST, PUT, DELETE, or PATCH Methods)**

If you are using a method other than GET, you need to include additional data with your API request in the "Request body" field.

Enter the required information as per the API documentation, typically in JSON format.\
\
Example:\
For a POST request to the dummy JSON endpoint, the request body might look like this:

```javascript
{  
  "title": "foo",  
  "body": "bar",  
  "userId": 1  
}   
```

#### **Step 6: Handle Pagination (Optional)**

If your API returns data in multiple pages, enable the "Handle pagination" checkbox. Configure the pagination parameters, such as the page number and page size, according to the API documentation. Uniquery will automatically handle the pagination and retrieve all data across multiple requests.

**1. Offset Limit in URL**

For APIs that use offset and limit parameters in the URL, you can specify these parameters to control pagination.

* **Example API**: `https://api.example.com/data?offset=0&limit=50`
* **Pagination Parameters**:
  * **Offset Parameter**: `offset`
  * **Limit Parameter**: `limit`
  * **Limit Value**: `50`

**2. Offset Limit in Request Body**

Some APIs require offset and limit parameters to be included in the request body.

* **Example API**: `https://api.example.com/data`
*   **Request Body**:

    ```javascript
    {  
      "offset": 0,  
      "limit": 50  
    }  
    ```
* **Pagination Parameters**:
  * **Offset Parameter**: `offset`
  * **Limit Parameter**: `limit`
  * **Limit Value**: `50`

**3. Cursor in URL**

APIs using cursors typically provide a token that you include in the URL to retrieve the next set of results.

* **Example API**: `https://api.example.com/data?cursor=abcdef`
* **Pagination Parameters**:
  * **Cursor Parameter**: `cursor`
  * **Cursor Path in Response**: `data.nextCursor`

**4. Cursor in Response Body**

For APIs that return the cursor in the response body, you need to specify the cursor path.\


* **Example API**: `https://api.example.com/data`
*   **Response Body**:

    ```javascript
    {  
      "data": [...],  
      "nextCursor": "abcdef"  
    }  
    ```
* **Pagination Parameters**:
  * **Cursor Parameter**: `cursor`
  * **Cursor Path in Response**: `nextCursor`

**5. Next Page URL in Response**

Some APIs provide the URL for the next page of results directly in the response.

* **Example API**: `https://api.example.com/data`
*   **Response Body**:

    ```javascript
    {  
      "data": [...],  
      "nextPageUrl": "https://api.example.com/data?page=2"  
    }  
    ```
* **Pagination Parameters**:
  * **Next Page URL Path**: `nextPageUrl`

**6. Page-Based Pagination in URL**

APIs using page-based pagination typically have parameters for the page number and page size.\


* **Example API**: `https://api.example.com/data?page=1&pageSize=50`
* **Pagination Parameters**:
  * **Page Parameter**: `page`
  * **Page Size Parameter**: `pageSize`
  * **Page Size Value**: `50`

**7. Page-Based Pagination in Request Body**

For APIs that use page-based pagination and require the parameters in the request body.\


* **Example API**: `https://api.example.com/data`
*   **Request Body**:

    ```javascript
    {  
      "page": 1,  
      "pageSize": 50  
    }  
    ```
* **Pagination Parameters**:
  * **Page Parameter**: `page`
  * **Page Size Parameter**: `pageSize`
  * **Page Size Value**: `50`

#### Setting Stop Conditions

To ensure efficient pagination handling, you can set stop conditions such as:

* **Max Page Reached**: Specify the maximum number of pages to retrieve.
* **No Data is Returned**: Pagination stops when the API response contains no data.
* **A Specific Field is Empty**: Specify a field path that indicates when pagination should stop if the field is empty.

By configuring these parameters and conditions, Uniquery will manage the pagination process automatically, ensuring comprehensive data retrieval across multiple requests. This functionality allows you to handle large datasets effectively and focus on analyzing the data

\
\
