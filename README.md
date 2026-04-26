# Enterprise Data Warehouse with SAP BW/4HANA

**ISOM 230 — Spring 2026 — Suffolk University**

> Benedict Daxell Santoso — Project Leader

A complete, end-to-end enterprise data warehouse project built on SAP BW/4HANA 2.0, covering the full business intelligence lifecycle from raw data ingestion to predictive forecasting. Built for Global Bike Inc. (GBI), a fictional multinational bicycle company operating across Germany and the US.

<img width="2502" height="1295" alt="ETL _SAP HANA banner" src="https://github.com/user-attachments/assets/d7b21f23-e331-47db-9ef6-ada284d58cc3" />

**Live portfolio site:** [bdsantoso168.github.io/Enterprise-Data-Warehouse-with-SAP-BW-4HANA](https://bdsantoso168.github.io/Enterprise-Data-Warehouse-with-SAP-BW-4HANA/)

---

## What was built

| Layer | Object | Description |
|---|---|---|
| Extraction | DataSources (DE + US) | Locale-aware ingestion of 171,012 raw sales records |
| Modeling | InfoObjects | Key figures (Revenue, Sales Qty) and characteristics (Material, Product Category) |
| Master Data | Material ETL flow | Two-step attribute and text load for 29 materials |
| Data Warehouse | aDSO BD1DM1026 | Structured fact store across 5 dimension groups |
| Reporting | CompositeProvider BD1CP1026 | Virtual reporting layer with navigation attributes |
| Dashboard | SAP Lumira Designer | Interactive executive dashboard with filters and charts |
| Forecasting | SAP Predictive Analytics | Triple Exponential Smoothing model for 2012 revenue forecast |

---

## Project benchmarks

| Benchmark | Topic | Status |
|---|---|---|
| BM2 | Data acquisition — DataSource design and extraction | Complete |
| BM3 | InfoObject modeling — key figures and characteristics | Complete |
| BM4 | Master data load — material attributes and texts | Complete |
| BM5 | Enterprise data warehouse build — aDSO and transformations | Complete |
| BM6 | BI reporting — CompositeProvider and sales reports | Complete |
| BM7 | Executive dashboard — SAP Lumira Designer | Complete |
| BM8 | Predictive analytics — time series forecasting | Complete |

---

## Key numbers

- **171,012** sales transactions loaded across Germany and the US
- **29** materials with full attribute and text master data
- **$88.8B+** in total revenue queryable across product, customer, and time dimensions
- **$41.4B+** in cost of goods manufactured data modeled for analytics
- **8 / 8** benchmarks completed across the full BI lifecycle

---

## Tech stack

- SAP BW/4HANA 2.0
- SAP Eclipse Modeling Tools
- SAP Fiori (BW Cockpit)
- SAP Lumira Designer
- SAP Predictive Analytics (Expert Analytics)

---

## Repo structure

```
/
├── index.html                        # Live portfolio page
├── README.md                         # This file
├── docs/
│   ├── BD1DB1026.zip                 # SAP Lumira dashboard export (BM7)
│   ├── BD1026_BikeAnalysisModel.lums # SAP PA predictive model (BM8)
│   └── ISOM230_FinalReport.pdf       # Team project report (coming soon)
├── bm2_de_preview.png
├── bm2_us_preview.png
├── bm3_revenue_infoobject.png
├── bm3_material_infoobject.png
├── bm4_data_flow.png
├── bm4_attributes.png
├── bm4_texts.png
├── bm4_dtp_monitor.png
├── bm5_adso_structure.png
├── bm5_data_flow.png
├── bm6_composite_provider.png
├── bm6_report.png
├── bm7_dashboard.png
├── bm7_chart.png
└── bm8_timeseries.png
```

---

## ETL pipeline overview

**Extract** — Designed two DataSources with locale-specific handling for German (comma decimal, EUR) and US (period decimal, USD) flat file formats. Configured field types, data lengths, and conversion routines before loading.

**Transform** — Mapped raw DataSource fields to semantically rich InfoObjects. Applied formula rules (Net Sales = Revenue minus Discount), constant language key rules, and a time-dependent master data lookup to derive Sales Organization from Customer master data.

**Load** — Executed Data Transfer Processes (DTPs) to load 29 material master records and 171,012 sales transactions into the aDSO. Activated requests via BW Cockpit for reporting availability.

---

*ISOM 230, Spring 2026 — all 8 benchmarks delivered*
