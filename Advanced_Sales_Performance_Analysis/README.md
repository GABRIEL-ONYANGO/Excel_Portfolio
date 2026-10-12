# Advanced Sales Dashboard (Excel)

An interactive Excel sales dashboard built on 2,000 retail orders for 2026. It uses PivotTables, PivotCharts, slicers and a timeline so you can filter revenue, orders and product performance by region, channel, customer type, category and date.

**File:** `Advanced_Sales_Dashboard.xlsx`

## Dashboard at a Glance

The **Dashboard** sheet meets the requirements listed in the workbook's *Dashboard Requirements* sheet.

| Requirement | How it is shown |
|-------------|-----------------|
| Total Revenue | KPI card (linked to `Pivot Analysis!A4`) |
| Total Orders | KPI card (linked to `Pivot Analysis!C4`) |
| Quantity Sold | KPI card (linked to `Pivot Analysis!E4`) |
| Average Order Value | KPI card (linked to `Pivot Analysis!G4`) |
| Monthly Revenue Trend | Line chart |
| Regional Performance | Column chart: Revenue by Region |
| Product Category Performance | Column chart: Revenue by Product Category |
| Sales Channel Contribution | Doughnut chart: Revenue by Sales Channel |
| Top Products by Revenue | Bar chart: Top 5 Products |

### Interactive Filters

- **Slicers:** Region, Sales Channel, Customer Type, Product Category
- **Timeline:** Date, with Years, Quarters, Months and Days levels

All slicers and the timeline are connected to the pivot tables, so the KPIs and charts update together.

## Workbook Structure

| Sheet | Purpose |
|-------|---------|
| `Sales Data` | Raw order data (2,000 rows, 12 columns) |
| `Pivot Analysis` | Nine PivotTables that feed the KPI cards and charts |
| `Dashboard` | Final presentation layer: KPI cards, 5 charts, slicers, timeline |
| `Clean Data` | Cleaned copy of the data, formatted as the Excel Table `Sales_Data_Table`. This is the pivot source. |
| `Dashboard Requirements` | The checklist of metrics and visuals the dashboard covers |

## Data Dictionary

| Column | Description |
|--------|-------------|
| Order ID | Unique order identifier (`ORD-1001` onward) |
| Date | Order date, 1 Jan 2026 to 31 Dec 2026 |
| Region | Central, East, North, South, West |
| Sales Channel | Corporate Sales, Marketplace, Online, Retail Store |
| Customer Type | New, Returning |
| Product Category | Accessories, Computers, Monitors, Networking, Office Supplies, Storage |
| Product | 28 distinct products (e.g. Gaming Laptop, Wi-Fi Router, Mouse Pad) |
| Salesperson | 15 salespeople |
| Quantity | Units sold |
| Unit Price | Price per unit |
| Discount | Discount rate applied (e.g. 0.05 = 5%) |
| Revenue | `Quantity × Unit Price × (1 − Discount)` |

## Data Quality

- 2,000 orders, no missing values and no duplicate Order IDs
- Revenue matches `Quantity × Unit Price × (1 − Discount)` on every row
- The `Region` column header has a trailing space (`"Region "`). It is kept as-is because the pivot tables and slicer reference that name.

## Headline Figures (unfiltered)

| Metric | Value |
|--------|-------|
| Total Revenue | $2,452,084 |
| Total Orders | 2,000 |
| Quantity Sold | 5,552 |
| Average Order Value | $1,226 |
| Top product | Gaming Laptop ($432,576) |

The currency symbol is assumed; check the cell formats in the workbook.

## How to Use

1. Open `Advanced_Sales_Dashboard.xlsx` in desktop Excel 2013 or later. The timeline and slicers are not supported in Excel for the web or other spreadsheet apps.
2. Go to the **Dashboard** sheet.
3. Click slicer buttons (hold `Ctrl` to multi-select) or drag the timeline to filter. Use the clear-filter icon on a slicer to reset it.
4. To refresh after changing data, edit `Clean Data`, then choose **Data > Refresh All**.

## Notes

- The timeline carries the warning: *do not move or resize*.
- The dashboard sheet also contains a decorative 3D model and icon graphics.
- If you add rows, extend `Sales_Data_Table` (typing directly below it does this automatically) so the pivots pick up the new data.

## Built With

- Microsoft Excel: PivotTables, PivotCharts, slicers, timeline, Excel Tables, linked text boxes

## License

Add a license of your choice (e.g. MIT) before publishing.
