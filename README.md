# TASK-4-SALES-DASHBOARD

Walmart Weekly Sales Dashboard – Power BI

 Dataset Information

Dataset Name: Walmart_Sales.csv
Rows: 6435
Columns: 8
Stores Covered: 45
Period: 05-Feb-2010 → 26-Oct-2012

Columns Description
Column Name	Description
Store	Store ID number
Date	Week ending date
Weekly_Sales	Total sales for that week at the store
Holiday_Flag	1 = Major holiday week, 0 = Normal week
Temperature	Avg temperature in the region
Fuel_Price	Fuel cost in that region
CPI	Consumer Price Index
Unemployment	Unemployment rate
Dataset Summary (Auto-Calculated from Data)

Total Sales: $6,737,218,987

Average Weekly Sales: $1,046,964

Total Stores: 45

Total Weeks: 6435 records

 Project Objectives

The dashboard aims to:

Provide a complete business overview for all Walmart stores

Enable store comparison and performance ranking

Visualize sales trends over time

Compare holiday vs non-holiday sales

Enhance decision-making through interactive filters

Demonstrate professional Power BI dashboard design

Key KPIs (Displayed as Cards)

These KPIs form the top section of the dashboard:

Total Sales

Average Weekly Sales

Store Count

Holiday Sales

Non-Holiday Sales

Holiday Sales %

Best Performing Store (optional)

🧠 DAX Measures Used
1. Total Sales
Total Sales = SUM('Walmart_Sales'[Weekly_Sales])

2. Average Weekly Sales
Average Weekly Sales = AVERAGE('Walmart_Sales'[Weekly_Sales])

3. Store Count
Store Count = DISTINCTCOUNT('Walmart_Sales'[Store])

4. Holiday Sales
Holiday Sales = 
    CALCULATE(
        [Total Sales],
        'Walmart_Sales'[Holiday_Flag] = 1
    )

5. Non-Holiday Sales
Non Holiday Sales = 
    CALCULATE(
        [Total Sales],
        'Walmart_Sales'[Holiday_Flag] = 0
    )

6. Holiday Sales %
Holiday Sales % = DIVIDE([Holiday Sales], [Total Sales])

 Dashboard Visuals
1. KPI Cards (Top Row)

Total Sales

Average Weekly Sales

Store Count

Holiday Sales %

Best Store (optional)

2. Line Chart – Sales Trend Over Time

Axis: Date

Values: Total Sales

Shows seasonality, growth, peaks, declines.

3. Bar Chart – Sales by Store

Axis: Store

Values: Total Sales

Sorted DESC by sales

Helps identify top-performing stores.

4. Column Chart – Holiday vs Non-Holiday Sales

Axis: Holiday_Flag

Values: Total Sales

Shows how holidays impact sales.

5. Table – Detailed Records

Columns:

Date

Store

Weekly_Sales

Holiday_Flag

Temperature

Fuel_Price

CPI

Unemployment

Useful for drill-down analysis.

 Interactivity (Slicers)

The dashboard includes:

Date Range Slicer (Between)

Store Slicer (Dropdown)

Holiday Slicer (Holiday / Normal Week)

All visuals cross-filter each other for a full interactive experience.

---- Design & Theme

Professional design guidelines followed:

Clean blue/white theme

Minimal clutter

Consistent color palette

Clear titles & labels

Highlights for KPIs

Organized 3-section layout (KPIs → Visuals → Table)
