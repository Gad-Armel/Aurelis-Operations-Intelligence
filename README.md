# Aurelis Operations Intelligence

Aurelis is an R Shiny decision-support application for commercial and supply-chain
teams. It brings sales, customers, quotations, purchasing, inventory, receivables,
and analytical reporting into one operational workspace.

The included company records are synthetic demonstration data. The application
supports analysis and investigation but does not replace accounting, ERP,
warehouse, identity, or authorization systems.

## Real-world problems addressed

- Identify revenue and margin pressure across customers and reporting periods.
- Review receivables exposure, overdue balances, and collection priorities.
- Monitor purchase orders, buyer workload, supplier risk, and delivery schedules.
- Investigate inventory, backorders, and fulfillment constraints.
- Explore datasets, test hypotheses, forecast trends, and build presentations.

## Main capabilities

- Executive overview and KPI command center.
- Customer, sales, receivables, and purchase-order analysis.
- Supplier, inventory, delivery, and buyer-workload monitoring.
- CSV, TSV, Excel, RDS, and JSON data exploration.
- Statistical profiles, comparisons, regression, forecasting, and scenarios.
- PDF and spreadsheet-oriented report workflows.

## Run locally

Open `Business Operation Intelligent Platform.Rproj` in RStudio and run:

```r
shiny::runApp(".")
```

No Node.js, Python, external database, or external AI service is required.

## Validation

From the project root:

```r
source("tests/validate_workspace.R")
source("tests/smoke_app.R")
```

The application currently uses demonstration data and should not be treated as a
production accounting or operational control system.
