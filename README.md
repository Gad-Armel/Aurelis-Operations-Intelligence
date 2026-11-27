# Aurelis Operations Decision Intelligence

Aurelis is an R Shiny decision-support platform that helps commercial and supply-chain teams turn fragmented operational data into a consistent management workflow. It connects sales, customers, quotations, purchasing, inventory, receivables, suppliers, and reporting in one analytical workspace.

## Real-world problem

Operational leaders often make decisions across disconnected spreadsheets, inconsistent definitions, and delayed reports. This slows the response to margin pressure, overdue receivables, supply constraints, supplier risk, and fulfillment issues.

Aurelis addresses that problem by giving teams a shared view of performance, drill-down analysis, data exploration, and repeatable reporting—while clearly distinguishing demonstration analytics from production systems of record.

## Business capabilities

- Executive KPI monitoring and period-based performance review.
- Customer, sales, quotation, and margin analysis.
- Receivables exposure, overdue balances, and collection prioritization.
- Purchase-order, supplier, buyer-workload, and delivery monitoring.
- Inventory, backorder, and fulfillment investigation.
- CSV, TSV, Excel, RDS, and JSON data exploration.
- Statistical profiles, comparisons, regression, forecasting, scenarios, and report workflows.

## Technology and skills demonstrated

- **Language and framework:** R, Shiny, bs4Dash.
- **Data and analysis:** dplyr, tidyr, readxl, openxlsx, jsonlite, statistical profiling, regression, forecasting, and scenario analysis.
- **Visualization and interaction:** ggplot2, Plotly, DT, Leaflet, HTML, CSS, and JavaScript.
- **Engineering:** modular R organization, reactive state management, KPI definition, data-quality checks, export workflows, and validation scripts.
- **Professional practice:** transparent assumptions, source-aware analysis, reproducible local execution, and explicit prototype boundaries.

## Run locally

Open `Business Operation Intelligent Platform.Rproj` in RStudio, then run:

```r
shiny::runApp(".")
```

Validation scripts are available in `tests/`:

```r
source("tests/validate_workspace.R")
source("tests/smoke_app.R")
```

## Data and production boundaries

The included company records are synthetic demonstration data. The application does not replace accounting, ERP, warehouse, identity, or authorization systems. Production use requires validated source definitions, access controls, data governance, and business-owner approval.