# Real Estate Sales Dashboard (Power BI)

An interactive Power BI dashboard that answers three questions: where does the profit come from, which property types earn the most, and who drives sales.

![Dashboard](screenshots/dashboard.png)

## Key findings
- 252M in sales, 157M in cost and 95M in profit, a 37.8% margin
- 4,269 properties sold across about 3,290 sales records
- 1-bedrooms sell the most units (1,565) but earn only 25% of the profit; 2-bedrooms earn 42%
- Musa closed 94M, more than a third of total sales; Tulika closed 25M
- Austin (83M), Orlando (79M) and Beverly Hills (78M) lead; Denver is about 5% of sales (13M), and 196 of its 285 sales are 1-bedrooms

More detail and where each number comes from: [docs/insights.md](docs/insights.md)

## What's in the dashboard
| Section | Visual |
|---|---|
| KPI cards | No. of Houses, Qty Sold, Sales Total, Cost Total, Profit |
| Filters | Location slicer and Month slicer, both filter the whole page |
| Sales by Location | Bar chart |
| Profit by Property Type | Donut chart with amount and percentage |
| Sales by Salesperson | Column chart |
| Property Distribution | Treemap, Location then Property Type |
| Sales and Profit by Month | Line chart |
| Property Bedroom Analysis | Matrix of quantity sold by location and property type, with totals |

## How it's built
- **Model:** a `Data` table (sales records) and a `Measuress` table that holds the measures
- **Measures** in `Measuress`: `Total Houses`, `Total Qty`, `Total Selling`, `Total Cost`, `Total Profit` (see [dax/measures.md](dax/measures.md))
- **Month column** in `Data`, used by the Month slicer and the monthly line chart
- **Design:** a custom dark background with gradient KPI cards, and a defined colour palette (see [assets/color-palette.md](assets/color-palette.md))

## How to open
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
2. Open `dashboard/real-estate-sales-dashboard.pbix`.

The data is stored inside the `.pbix` file, so nothing else is needed.

## Repository structure
```
├── README.md
├── dashboard/        Power BI file
├── screenshots/      Dashboard image
├── dax/              Measure definitions
├── docs/             Insights and data dictionary
├── assets/           Background, icon and colour palette
└── data/             Source data notes
```

## Tools
Power BI Desktop, DAX
