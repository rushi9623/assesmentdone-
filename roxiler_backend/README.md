# roxiler-backend
Rushikesh Ughade
This project aims to implement a backend system to manage and analyze product transactions. The backend is designed to interact with a third-party API to fetch product transaction data, and it provides various APIs for listing transactions, generating statistics, and creating charts based on the fetched data.


## API Endpoints

### List All Transactions

- **Endpoint:** `/transactions`
- **Method:** `GET`
- **Description:** Lists all transactions based on the provided search parameters and pagination.
  - **Query Parameters:**
    - `month` (required): The month to filter transactions.
    - `search` (optional): Search text to match against product title/description/price.
    - `page` (optional): Page number for pagination (default: 1).
    - `perPage` (optional): Number of records per page (default: 10).

### Statistics

- **Endpoint:** `/statistics`
- **Method:** `GET`
- **Description:** Provides statistics for the selected month.
  - **Query Parameters:**
    - `month` (required): The month to retrieve statistics.

### Bar Chart

- **Endpoint:** `/bar-chart`
- **Method:** `GET`
- **Description:** Generates data for a bar chart, showing the price range and the number of items in each range for the selected month.
  - **Query Parameters:**
    - `month` (required): The month to generate the bar chart.

### Pie Chart

- **Endpoint:** `/pie-chart`
- **Method:** `GET`
- **Description:** Generates data for a pie chart, showing unique categories and the number of items from each category for the selected month.
  - **Query Parameters:**
    - `month` (required): The month to generate the pie chart.

### Combined Data

- **Endpoint:** `/combined-data`
- **Method:** `GET`
- **Description:** Fetches data from all the above APIs and combines the responses.

## How to Use

To interact with the APIs, make HTTP requests to the specified endpoints with the required parameters. Ensure that the `month` parameter is provided in all relevant requests.



