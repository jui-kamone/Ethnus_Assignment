# MERN Stack Coding Challenge Documentation 

## Overview

This project is a full-stack application built using the MERN stack, which includes MongoDB, Express.js, React.js, and Node.js. It features both backend and frontend components to manage and display transaction data fetched from a third-party API. The backend provides APIs to list transactions, generate statistics, and create bar and pie charts. The frontend uses these APIs to display data in a user-friendly web interface, allowing users to search transactions, view statistics, and see visual representations of the data.

## Backend

### Swagger Docs

- [Swagger Docs link](https://roxciler-systems-assement.onrender.com/api-docs/)


## API Endpoints
### 1. Initialization API

- **Endpoint:** `/api/v1/product/initialize-seed-data`
- **Method:** GET
- **Description:**  Fetches transaction data from the third-party API (`https://s3.amazonaws.com/roxiler.com/product_transaction.json`)and seeds the database.

### 2. List Products API

- **Endpoint:** `/api/v1/product`
- **Method:** GET
- **Description:**  Retrieves a list of transactions.
- **Parameters:**
- month (string): The month to filter  transactions.
- page (integer, optional): Page number for pagination (default: 1).
- perPage (integer, optional): Items per page - for pagination (default: 10).
- search (string, optional): Text to search in title/description/price.

### 3. Statistics API

- **Endpoint:** `/api/v1/analytics/statistics`
- **Method:** GET
- **Description:** Provides statistics for the specified month.
- **Parameters:**
  - `month` (string): The month for which statistics need to be fetched.

### 4. Bar Chart API

- **Endpoint:** `/api/v1/analytics/bar-chart`
- **Method:** GET
- **Description:** Generates bar chart data for the specified month.
- **Parameters:**
  - `month` (string): The month for which bar chart data needs to be fetched.

### 5. Pie Chart API

- **Endpoint:** `/api/v1/analytics/pie-chart`
- **Method:** GET
- **Description:** Generates pie chart data for the specified month.
- **Parameters:**
  - `month` (string): The month for which pie chart data needs to be fetched.

### 6. Combined API

- **Endpoint:** `/api/v1/analytics/combined-chart`
- **Method:** GET
- **Description:** Combines data from the statistics, bar chart, and pie chart APIs into a single JSON response.

## Frontend

### Transactions Table

- **Description:** A table that displays transactions

- Month Selection: Dropdown menu for selecting a month (January to December).
- Default Month: March.
- Search Box: Filters transactions by matching text in title, description, or price.
- Pagination: Next and Previous buttons for navigating through pages.

### Screenshot

- ![screencapture(products)](https://github.com/jui-kamone/Ethnus_Assignment/assets/118176425/1cc81c62-73f5-44c5-9afc-953a42a0a348)


### Transactions Statistics

- **Description:** Displays total amount of sale, total sold items, and total not sold items for the selected month.

### Transactions Bar Chart

- **Description:**  Displays a bar chart showing the price range and the number of items in each range for the selected month.

###  Screenshot(Bar chart)

![bar_chart](https://github.com/jui-kamone/Ethnus_Assignment/assets/118176425/92aa2726-1bb6-4f5f-af24-9ce5bde8cca1)






