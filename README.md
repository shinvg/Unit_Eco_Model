# FMCG Unit Economics & SKU-Level Contribution Margin Model

[![Excel](https://img.shields.io/badge/Model-Microsoft_Excel-green.svg)](https://microsoft.com/excel)
[![Financial Modeling](https://img.shields.io/badge/Domain-Corporate_Finance_%26_Unit_Economics-blue.svg)](#)

## Executive Summary

This repository contains a dynamic **FMCG Unit Economics & SKU Contribution Margin Model** built in Microsoft Excel. The model evaluates profitability at the individual stock-keeping unit (SKU) and product category level, analyzing pricing structures, channel-wise trade discounts, direct Cost of Goods Sold (COGS), trade promotion expenditure, and fulfillment/distribution logistics.

The objective of this project is to model unit profitability across distribution channels (Modern Trade, General Trade / Traditional Retail, and Direct-to-Consumer / E-Commerce), calculate break-even volumes, and assess channel margin structures for consumer packaged goods (CPG/FMCG).

---

## Key Highlights & Model Metrics

* **Core Focus:** SKU Unit Costing, Net Realization Rates, Trade Margin Structure, Channel Economics, and Contribution Margin Analysis.
* **Blended Gross Margin:** `~45.0%` (Gross Profit / Net Revenue)
* **Blended Contribution Margin 1 (CM1):** `~32.0%` (After direct variable costs & logistics)
* **Blended Contribution Margin 2 (CM2):** `~20.0%` (After performance marketing & trade promotions)
* **Key Channels Modeled:** 
  * **General Trade (GT):** Distributor + Retailer margin split.
  * **Modern Trade (MT):** Key Account terms, slotting fees, and listing allowances.
  * **D2C / E-Commerce:** Customer Acquisition Cost (CAC), payment gateway fees, third-party logistics (3PL) fulfillment.

---

## Model Architecture & Structure

The workbook is structured into modular tabs for clear analysis and presentation:

1. **Dashboard & Executive Summary:** High-level executive view featuring SKU margin waterfall charts, channel mix metrics, and contribution margin comparisons.
2. **SKU & Volume Assumptions:** Master data tab containing MSRP/MRP, pack sizes, volume growth rates, and SKU product category mappings.
3. **Channel Waterfall & Pricing Schedule:** Calculates Net Realized Price per unit from Maximum Retail Price (MRP) after subtracting retailer margins, distributor margins, and trade schemes.
4. **COGS Breakdown Schedule:**
   * **Bill of Materials (BOM):** Raw Materials (RM) and Packaging Materials (PM) per unit.
   * **Conversion Costs:** Direct contract manufacturing / co-packing expenses and factory processing fees.
5. **Logistics & Trade Marketing Engine:** Inbound/outbound freight per unit, warehousing fees, damage/return allowances, and channel-specific trade promotions.
6. **Sensitivity & Breakeven Matrix:** Evaluates CM2 impact across variations in raw material commodity inflation vs. price increases (MRP revisions).

---

## Unit Economics Waterfall Framework (Per Pack Base Case)

Below is an illustrative unit waterfall for a benchmark SKU across distribution channels:

| Metric / Line Item | General Trade (GT) | Modern Trade (MT) | Direct-to-Consumer (D2C) | Blended Average |
| :--- | :---: | :---: | :---: | :---: |
| **Maximum Retail Price (MRP)** | `$10.00` | `$10.00` | `$10.00` | `$10.00` |
| **(-) Channel Margins & Discounts** | `($2.50)` | `($3.20)` | `($0.00)` | `($2.30)` |
| **Net Revenue / Realization** | **`$7.50`** | **`$6.80`** | **`$10.00`** | **`$7.70`** |
| **(-) Raw & Packaging Material (BOM)**| `($2.80)` | `($2.80)` | `($2.80)` | `($2.80)` |
| **(-) Conversion & Co-Packing Costs** | `($0.70)` | `($0.70)` | `($0.70)` | `($0.70)` |
| **Gross Profit per Unit** | **`$4.00`** | **`$3.30`** | **`$6.50`** | **`$4.20`** |
| **Gross Margin (%)** | **`53.3%`** | **`48.5%`** | **`65.0%`** | **`54.5%`** |
| **(-) Logistics, Freight & Packaging** | `($0.50)` | `($0.60)` | `($2.10)` | `($0.90)` |
| **Contribution Margin 1 (CM1)** | **`$3.50`** | **`$2.70`** | **`$4.40`** | **`$3.30`** |
| **(-) Trade Promo / Ad Spend (CAC)** | `($0.80)` | `($1.10)` | `($2.50)` | `($1.30)` |
| **Contribution Margin 2 (CM2)** | **`$2.70`** | **`$1.60`** | **`$1.90`** | **`$2.00`** |
| **CM2 % (on Net Realization)** | **`36.0%`** | **`23.5%`** | **`19.0%`** | **`26.0%`** |

*(Note: Replace placeholder figures with exact numbers from your Excel workbook.)*

---

## Sensitivity Analysis

The model evaluates how unit Contribution Margin (CM2 %) responds to fluctuating **Raw Material Inflation (%)** vs. **Retail Price Changes (MRP Adjustments %)**.

### CM2 Margin Sensitivity Matrix (%)

| Raw Material Price Delta \ MRP Change | -5% Price Cut | 0% (Current MRP) | +5% Price Hike |
| :---: | :---: | :---: | :---: |
| **+10% RM Inflation** | `20.1%` | `22.8%` | `25.3%` |
| **0% RM Inflation (Base)** | `23.4%` | **`26.0%`** | `28.4%` |
| **-10% RM Deflation** | `26.7%` | `29.1%` | `31.4%` |

---

## Repository Structure

```text
├── FMCG_Unit_Economics_Model.xlsx   # Full Excel Model (BOM, Channel Waterfall, CM1/CM2 Engine)
├── README.md                        # Project documentation and summary
