# 📊 Financial Dashboard — Distribuidora Rojas Hermanos

**Automated P&L, cash flow, and margin tracking for a 3-branch Mexican FMCG distributor.**

Built as a freelance BI project. Raw data came from 3 completely different sources — an Aspel SAE export, a manually filled Excel, and the owner's own expense sheet. Cleaned, modeled, and delivered as a live Power BI dashboard connected to SharePoint in 1 week.

→ **[Full case study on Notion](https://www.notion.so/Automated-Financial-Dashboard-Mexican-FMCG-Distributor-365b7682d7a780808311d39841913f80)** — problem, process, DAX measures, and results.

---

## Project Structure

```
DISTRIBUIDORA-ROJAS-HERMANOS/
│
├── data/
│   ├── _raw/                          # Original files as received from client
│   │   ├── ventas_CDMX_aspel_export.xlsx
│   │   ├── ventas_GDL_lupita_manual.xlsx
│   │   ├── gastos_operativos_dueño.xlsx
│   │   └── compras_proveedores.xlsx
│   │
│   └── processed/                     # Cleaned, standardized templates
│       ├── ventas_CDMX.xlsx
│       ├── ventas_GDL.xlsx
│       ├── gastos_operativos_CDMX_Norte.xlsx
│       ├── gastos_operativos_CDMX_Sur.xlsx
│       ├── gastos_operativos_Guadalajara.xlsx
│       └── presupuestos.xlsx
│
├── notebooks/
│   └── clean_data.ipynb               # EDA and initial data profiling
│
└── reports/
    └── dashboard_dist_rojas_hermanos.pbix
```

---

## Data Challenges

The raw data had real-world messiness across all 3 sources:

- Aspel export with 3-row system headers, `N/D` values, duplicated rows
- Manual Excel with amounts as text (`$1,234.00`), 4 mixed date formats, subtotal rows inside transaction data
- No payment status tracking in the Guadalajara branch (12+ months of unverified receivables)
- Owner's expense file with swapped month/day dates and occasional duplicates

---

## Dashboard

![Descripción de la imagen](reports/Dashboard-Screenshot.png "Hi")

- P&L with MoM and YoY deltas
- Cash flow waterfall + accumulated trend
- Margin by branch
- Operating expenses with budget alert (turns red when over threshold)
- Payment status breakdown
- Cancelled sales tracker
- Filters by branch, year, and month

---

## Context

This was a freelance engagement for a real-world business scenario. The owner had no financial visibility beyond a monthly PDF from their accountant. The goal was daily visibility, not just prettier spreadsheets.
