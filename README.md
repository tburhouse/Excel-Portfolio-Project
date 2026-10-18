# UK Online Retail Analysis — Excel

## Project question
How did positive invoiced sales change across January–November 2011, which countries contributed the most sales value, and how many identifiable customers placed multiple orders?

## Tools and data
Microsoft Excel, Power Query, PivotTables and a chart. The source is the original Online Retail Excel workbook; this project uses a separate working copy for the analysis.

## Data preparation
- Audited the 541,909 source lines for cancellations, negative quantities, nonpositive prices and missing CustomerID values.
- Used Power Query to keep lines dated January–November 2011 with Quantity > 0 and UnitPrice > 0. Calculated SalesValueGBP as Quantity × UnitPrice, leaving 463,513 prepared sales lines.
- For customer invoice counts, kept rows with a CustomerID, removed duplicate CustomerID–InvoiceNo pairs, then counted distinct invoices per customer.

## Findings
- Positive invoiced sales value totalled £9,204,145.72 across January–November 2011. Monthly value rose from August through November, reaching £1.51m in November.
- The UK accounted for 83.49% of this sales value. EIRE and the Netherlands followed at 2.89% and 2.88%.
- Of 4,173 identifiable customers, 62.90% had two or more distinct positive-sales invoices during the period.

## Limitations
This measures positive invoiced sales value, not net revenue or profit; returns and cancellations are excluded. Customer findings exclude records without a CustomerID. Having two or more invoices within this period is not a customer retention rate.

## Source and reproduction
Source: Chen, D. (2015). Online Retail [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33. Licensed CC BY 4.0.

1. Open `UK_Online_Retail_Analysis.xlsx`. The `Online Retail` sheet contains the source data used by the workbook.
2. Review the checks on `Audit` and the two Power Query queries under Data > Queries & Connections.
3. Select Data > Refresh All to update the prepared tables and PivotTables.
4. Open `Summary` for the results, then inspect `Monthly Sales`, `Country Sales` and `Customer Sales` for the supporting breakdowns.
