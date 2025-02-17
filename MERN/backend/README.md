# MERN Stack Coding Challenge - Backend

## Backend Overview
The backend of this project is built using Node.js and Express. It provides a set of APIs for initializing the database, fetching product transactions, and generating statistics and visualizations.

## API Endpoints

### Database Initialization
- **Endpoint**: `/api/initialize`
- **Method**: GET
- **Description**: Fetches data from the third-party API and initializes the database with seed data.

### Transaction Listing
- **Endpoint**: `/api/transactions`
- **Method**: GET
- **Parameters**: 
  - `month` (required): The month to filter transactions (January to December).
  - `page` (optional): The page number for pagination (default: 1).
  - `perPage` (optional): The number of transactions per page (default: 10).
  - `search` (optional): The search query to filter transactions by title, description, or price.
- **Description**: Returns a list of product transactions based on the provided parameters.

### Statistics
- **Endpoint**: `/api/statistics`
- **Method**: GET
- **Parameters**: 
  - `month` (required): The month to calculate statistics for.
- **Description**: Returns statistics for the selected month, including total sale amount, total sold items, and total unsold items.

### Bar Chart
- **Endpoint**: `/api/barchart`
- **Method**: GET
- **Parameters**: 
  - `month` (required): The month to generate the bar chart for.
- **Description**: Returns data for a bar chart showing the number of items in each price range for the selected month.

### Pie Chart
- **Endpoint**: `/api/piechart`
- **Method**: GET
- **Parameters**: 
  - `month` (required): The month to generate the pie chart for.
- **Description**: Returns data for a pie chart showing the number of items in each unique category for the selected month.

### Combined API
- **Endpoint**: `/api/combined`
- **Method**: GET
- **Parameters**: 
  - `month` (required): The month to fetch data for.
- **Description**: Returns a combined JSON response containing data from the transaction listing, statistics, bar chart, and pie chart APIs for the selected month.

## Getting Started
1. Initialize Your Node.js Project:
   ```bash
   mkdir backend
    cd backend
    npm init -y

2. Install Dependencies
    ```bash
       npm install express mongoose axios

3. Start the server:
    ```bash
     node server.js ("run your .js file in my case my file name is server.js ")
    
4. The backend will be available at http://localhost:3000/api

5. You can check you API's end pont working or not using POSTMAN software.
   here is the [link](https://www.postman.com/downloads/)
