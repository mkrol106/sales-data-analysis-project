# Sales data analysis project

## Project description
This is the practice data analysis project, aiming to gather insights and information from the messy and unprocessed sales data. Main tool for this project was python's pandas library, combined with several libraries for statistical computation and plotting. The whole code is accessible through the Jupyter Notebook platform.

## Technologies
The project was created with technologies, languages, platforms and libraries below:
- Python version 
  - pandas version
  - numpy version
  - matplotlib version
  - seaborn version
  - scipy version
- Jupyter Notebook version 

## Source of the data
The data for this project comes from Sales Product Dataset, hosted on kaggle under the url
https://www.kaggle.com/datasets/knightbearr/sales-product-data.
This dataset is split into 12 .csv files for each month of the year 2019. Many of those files contain missing rows, duplicated column names and incorrectly formatted data. All files contain the following columns:
- Order ID - An Order ID is the number system that Amazon uses exclusively to keep track of orders. Each order receives its own Order ID that will not be duplicated. This number can be useful to the seller when attempting to find out certain details about an order such as shipment date or status.
- Product - The product that have been sold.
- Quantity Ordered - Ordered Quantity is the total item quantity ordered in the initial order (without any changes).
- Price Each - The price of each products.
- Order Date - This is the date the customer is requesting the order be shipped.
- Purchase Address - The purchase order is prepared by the buyer, often through a purchasing department. The purchase order, or PO, usually includes a PO number, which is useful in matching shipments with purchases; a shipping date; billing address; shipping address; and the request items, quantities and price.

## Data processing
The whole process of cleaning and wrangling the source data was described and visualized in the notebook 01_data_processing. Sections below offer a brief synopsis of the applied changes.

### Data cleaning
At first, the data from many csv files was imported into a single pandas data frame for convenience. After the brief assessment, the following changes were applied:
- missing and duplicated rows were removed,
- rows with invalid data, such as rows with column names in value fields, were removed.

### Data wrangling
After the initial cleaning, the data frame of valid data was transformed into the desired formatting:
- "Order ID", "Quantity Ordered" and "Price Each" columns were converted to the correct numerical data types,
- "Order Date" column was converted to the correct datetime data type,
- new columns were added based on the existing columns for the later ease of working with the data:
  - from "Order Date", the "Order Month" and "Order Time" columns were extracted,
  - column "Purchase Address" was split into additional, more detailed information, such as state and city,
  - a new calculated column "Total Price" was created based on each product's unit price and ordered quantity,
- transformed data was split into two tables (data frames):
  - order_items data frame, for detailed information about each product in each order,
  - orders data frame, for detailed information about each order from the shipping perspective (no information about ordered products).

After transformation, the two resulting data frames were exported to csv files in a directory 'clean_data'.

## Data analysis









