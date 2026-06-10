# Sales Analytics Dashboard


## Project Overview

This project is an interactive Excel dashboard built to analyze e-commerce sales data spanning from January 2023 to June 2025. The dashboard transforms raw transaction data into actionable business insights through dynamic pivot tables, charts, and slicers.

The dashboard enables stakeholders to track sales performance, monitor order status, identify top products and customers, and evaluate marketing channel effectiveness.

---

## Dataset Summary

| Metric | Value |
|--------|-------|
| Total Orders | 1,200 |
| Date Range | Jan 2023 - Jun 2025 |
| Unique Customers | 1,200 |
| Total Revenue | $2,500,000+ |
| Product Categories | 7 |
| Payment Methods | 5 |
| Order Statuses | 5 |
| Referral Sources | 5 |

### Columns in Cleaned Dataset

| Column | Description |
|--------|-------------|
| OrderID | Unique order identifier |
| Date | Order date (YYYY-MM-DD) |
| CustomerID | Unique customer identifier |
| Product | Product category |
| Quantity | Number of units ordered |
| UnitPrice | Price per unit |
| PaymentMethod | Payment type used |
| OrderStatus | Current order status |
| CouponCode | Discount code applied |
| ReferralSource | Marketing channel |
| TotalPrice | Final order total |

### Product Categories
Monitor, Phone, Tablet, Chair, Printer, Laptop, Desk

### Order Statuses
Shipped, Delivered, Cancelled, Returned, Pending

### Payment Methods
Credit Card, Debit Card, Online, Cash, Gift Card

### Referral Sources
Email, Facebook, Instagram, Google, Referral

### Coupon Codes
SAVE10, FREESHIP, WINTER15, None

---

## Data Cleaning Process

The raw dataset was cleaned using Python before importing into Excel.

### Steps Performed

1. Removed unnecessary columns (TrackingNumber, ShippingAddress, ItemsInCart)
2. Converted Date column to YYYY-MM-DD format
3. Standardized text capitalization for all categorical columns
4. Filled empty CouponCode values with "None"
5. Rounded TotalPrice to 2 decimal places
6. Removed duplicate records
7. Sorted data by date

### Before vs After

| Aspect | Before | After |
|--------|--------|-------|
| Columns | 14 | 11 |
| Date format | 2023-01-04 00:00:00 | 2023-01-04 |
| Product names | MONITOR | Monitor |
| CouponCode blanks | (empty) | None |
| TotalPrice | 769.3799999999 | 769.38 |

---

## Dashboard Components

### Pivot Tables Created

| Pivot Table | Rows | Values |
|-------------|------|--------|
| Sales by Product | Product | Sum of TotalPrice, Count of Orders |
| Monthly Sales Trend | Date (Month) | Sum of TotalPrice |
| Order Status Distribution | OrderStatus | Count of Orders |
| Revenue by Referral Source | ReferralSource | Sum of TotalPrice |
| Coupon Performance | CouponCode | Sum of TotalPrice, Count of Orders |
| Payment Method Analysis | PaymentMethod | Sum of TotalPrice, Avg TotalPrice |
| Top Customers | CustomerID | Sum of TotalPrice |
| Product by Referral Source | ReferralSource, Product | Sum of TotalPrice |

### Charts Used

| Chart Type | Purpose |
|------------|---------|
| Column Chart | Monthly sales trends |
| Bar Chart | Product sales ranking |
| Pie Chart | Order status distribution |
| Horizontal Bar Chart | Referral source revenue |
| Donut Chart | Payment method share |
| Table | Top customers list |

### Slicers (Filters)

| Slicer | Filter Options |
|--------|----------------|
| Date | Month, Quarter, Year |
| Product | Monitor, Phone, Tablet, Chair, Printer, Laptop, Desk |
| Payment Method | Credit Card, Debit Card, Online, Cash, Gift Card |
| Order Status | Shipped, Delivered, Cancelled, Returned, Pending |
| Referral Source | Email, Facebook, Instagram, Google, Referral |
| Coupon Code | SAVE10, FREESHIP, WINTER15, None |

### Key Performance Indicators (KPIs)

| KPI | Formula |
|-----|---------|
| Total Revenue | SUM(TotalPrice) |
| Average Order Value | SUM(TotalPrice) / COUNT(OrderID) |
| Cancellation Rate | COUNT(Cancelled) / Total Orders |
| Return Rate | COUNT(Returned) / Total Orders |
| Delivery Success Rate | COUNT(Delivered) / Total Orders |
| Revenue per Customer | SUM(TotalPrice) / Unique Customers |
| Items per Order | SUM(Quantity) / COUNT(OrderID) |

---

## Key Insights

After analyzing the data, the following insights were discovered:

1. **Top Product:** Laptop generates the highest revenue among all product categories

2. **Peak Sales Month:** December shows the highest sales volume due to holiday season

3. **Order Status:** 70% of orders are successfully delivered or shipped, while 15% are cancelled and 15% returned

4. **Best Referral Source:** Instagram brings the highest revenue compared to other marketing channels

5. **Coupon Effectiveness:** SAVE10 is the most frequently used coupon code

6. **Popular Payment Method:** Credit Card is the preferred payment method among customers

---

## How to Use the Dashboard

1. Download the Sales_Dashboard.xlsx file

2. Enable Editing if prompted by Excel

3. Use Slicers to filter data:
   - Click any button on the slicers to filter
   - Hold Ctrl to select multiple options
   - Click the funnel icon to clear filters

4. Interact with Charts:
   - Hover over chart elements to see values
   - Click on legend items to show/hide categories
   - Right-click charts for additional options

5. Refresh Data:
   - Right-click any pivot table
   - Select Refresh
   - Or press Ctrl+Alt+F5

---

## Project Structure
