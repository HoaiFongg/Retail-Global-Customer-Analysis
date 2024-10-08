# 📊 Retail-Global-Customer-Analysis

## 🗂️ Data

The **Retail-Global-Customer-Analysis** project utilizes a dataset that includes three main sheets, each representing a key set of information:

### 1. **Order** 📝
Contains detailed information about customer orders. Key columns include:
- **Row ID**: Unique identifier for each row.
- **Order ID**: Unique order identifier.
- **Order Date**: Date the order was placed.
- **Ship Date**: Date the order was shipped.
- **Ship Mode**: Shipping method (Standard, First Class, Second Class, Same Day).
- **Customer ID**: Unique customer identifier.
- **Customer Name**: Name of the customer.
- **Segment**: Customer segment (Consumer, Corporate, Home Office).
- **Postal Code**: Customer's postal code.
- **City**, **State**, **Country**, **Region**: Geographic information of the customer.
- **Market**: Market region of the customer.
- **Product ID**: Unique product identifier.
- **Category**, **Sub-Category**: Product category and sub-category.
- **Product Name**: Name of the product.
- **Sales**: Revenue generated from the order.
- **Quantity**: Number of items sold.
- **Discount**: Discount applied to the order.
- **Profit**: Profit generated from the order.
- **Shipping Cost**: Shipping cost for the order.
- **Order Priority**: Priority level of the order.

### 2. **Return** 🔄
Contains information about returned orders:
- **Returned**: Return status (Yes/No).
- **Order ID**: Order ID of the returned order.
- **Region**: Geographic region of the returned order.

### 3. **People** 👥
Contains information about managers overseeing each region:
- **Person**: Name of the manager.
- **Region**: Region the manager is responsible for.

---

## 🔄 ETL Process in Power BI

### 1. ETL (Extract, Transform, Load)

#### 1.1 **Extract**
- Data from the **Order**, **Return**, and **People** sheets in the Excel file was imported into Power BI for further analysis.

#### 1.2 **Transform**
- **Data Cleaning**: Using **Power Query Editor**:
  - Removed any **null** values and ensured no missing data.
  - Reformatted date columns for consistency.
  - Verified and standardized **data types** for all columns, e.g., dates, numbers (sales, cost, profit), and identifiers.

#### 1.3 **Load**
- **Create DateDimension table**: An additional date table was created to support time-based analysis in the upcoming visualizations.

---

## 📈 Dashboard Creation

Once the ETL process was complete, the data was ready for analysis and visualization. The dashboard is divided into three main sections:

### 1. **Revenue and Profits** 💰
Analysis of revenue and profit:
- **Revenue by Customer**: Analyze revenue by **Customer ID** and **Customer Name** to identify top customers.
- **Profit by Product**: Use **Product ID** and **Product Name** to identify the most profitable products.
- **Overall Revenue & Profit**: Trend charts showing revenue and profit over time, segmented by market and customer type.
![Revenue and Profits Chart](images/Revenue%20and%20Profits.png)


### 2. **Analyze Shipping Costs** 🚚
Analysis of shipping costs and efficiency:
- **Shipping Time**: Use **Order Date** and **Ship Date** to calculate shipping duration and assess delivery performance.
- **Shipping Costs**: Compare **Shipping Cost** with order profits to evaluate cost efficiency.
- **Shipping Methods**: Create visual comparisons of different shipping methods such as **Standard Class**, **First Class**, and **Same Day**.
![Revenue and Profits Chart](images/Analyze%20and%20Shipping%20cost.png)


### 3. **Customer Segmentation** 👥
Analysis of customer segments:
- **Customer Segments**: Analyze revenue and profit by customer **Segment** (Consumer, Corporate, Home Office).
- **Customer Distribution by Region**: Geographic analysis using **Region** and **Country** columns.
- **Top Customers**: A list of top customers based on revenue and profit contribution.
![Revenue and Profits Chart](images/Customer%20segmentation.png)