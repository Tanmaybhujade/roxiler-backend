# roxiler-backend

This project aims to implement a backend system to manage and analyze product transactions. The backend is designed to interact with a third-party API to fetch product transaction data, and it provides various APIs for listing transactions, generating statistics, and creating charts based on the fetched data.

## Deployment

The project is deployed and can be accessed at  https://vercel.com/tanmaybhujades-projects/roxiler-backend-jkti. You can use the following APIs to interact with the system.

## API Endpoints

### Initialize Database

- **Endpoint:** `/api/initDatabase`
- **Method:** `GET`
- **Description:** Initializes the database by fetching JSON data from the third-party API and seeding the database with the received data.

### List All Transactions

- **Endpoint:** `/api/transactions`
- **Method:** `GET`
- **Description:** Lists all transactions based on the provided search parameters and pagination.
  - **Query Parameters:**
    - `month` (required): The month to filter transactions.
    - `search` (optional): Search text to match against product title/description/price.
    - `page` (optional): Page number for pagination (default: 1).
    - `perPage` (optional): Number of records per page (default: 10).

### Statistics

- **Endpoint:** `/api/statistics`
- **Method:** `GET`
- **Description:** Provides statistics for the selected month.
  - **Query Parameters:**
    - `month` (required): The month to retrieve statistics.

### Bar Chart

- **Endpoint:** `/api/bar-chart`
- **Method:** `GET`
- **Description:** Generates data for a bar chart, showing the price range and the number of items in each range for the selected month.
  - **Query Parameters:**
    - `month` (required): The month to generate the bar chart.

### Pie Chart

- **Endpoint:** `/api/pie-chart`
- **Method:** `GET`
- **Description:** Generates data for a pie chart, showing unique categories and the number of items from each category for the selected month.
  - **Query Parameters:**
    - `month` (required): The month to generate the pie chart.

### Combined Data

- **Endpoint:** `/api/combined-data`
- **Method:** `GET`
- **Description:** Fetches data from all the above APIs and combines the responses.

## How to Use

To interact with the APIs, make HTTP requests to the specified endpoints with the required parameters. Ensure that the `month` parameter is provided in all relevant requests.

Feel free to explore and analyze the product transactions using the provided APIs. If you have any questions or issues, please refer to the documentation or contact the project maintainers.

Enjoy using the product transaction management system!
