# E-Commerce Commercial Performance & Profitability Diagnostics

**Author:** Bhumika Chauhan  
**Domain:** Retail & E-Commerce Analytics  
**Tools:** Microsoft Power BI, DAX, Data Modelling, Data Analysis  
**Reporting Period:** FY 2018

---

## 1. Executive Summary

### Business Context

An Indian e-commerce retailer operating across 19 states recorded **₹437,771 in sales across 500 unique orders and 5,615 units** during FY 2018.

The analysis examines sales performance, profitability, product-category contribution, regional distribution, monthly trends and customer payment behaviour.

### Business Challenge

Despite generating ₹437,771 in sales, the business recorded ₹36,963 in profit, representing an overall profit-to-sales ratio of 8.44%.

The central analytical challenge was to identify:

- Which product categories contributed most to sales and profit?
- Which sub-categories recorded negative profitability?
- How concentrated was revenue across different states?
- Which months experienced the strongest and weakest profit performance?
- Which payment methods accounted for the largest transaction volume?

### Key Findings

The analysis identified several important commercial patterns:

- Five sub-categories recorded combined negative profit of **₹2,296**.
- Maharashtra and Madhya Pradesh contributed **43.39% of total sales**.
- Clothing generated higher profit than Electronics despite lower sales.
- COD accounted for **43.74% of total units sold**.
- November recorded the highest monthly profit, while May recorded the largest monthly loss.

These findings highlight opportunities for further investigation into product profitability, promotional performance, regional concentration and payment behaviour.

---

## 2. Analytical Methodology & Data Governance

### Data Architecture

The analysis uses two related datasets:

| Dataset | Purpose | Records |
|---|---|---:|
| Orders.csv | Order-level information | 500 |
| Details.csv | Transaction-level information | 1,500 |

**Orders.csv includes:**
- Order ID
- Order Date
- CustomerName
- State
- City

**Details.csv includes:**
- Order ID
- Amount
- Profit
- Quantity
- Category
- Sub-Category
- PaymentMode

The datasets are connected using **Order ID**, linking order-level information with transaction-level records.

### Data Quality Validation

The following checks were performed:

- 0 missing values across the supplied columns.
- 0 exact duplicate records in either dataset.
- 1,500 out of 1,500 transaction records matched an order ID.
- 500 unique order IDs in the Orders dataset.

### KPI Standardisation

The full-year business metrics were calculated using the supplied CSV files.

| KPI | FY 2018 Result |
|---|---:|
| Total Sales | ₹437,771 |
| Total Profit | ₹36,963 |
| Total Quantity | 5,615 |
| Unique Orders | 500 |
| Average Order Value | ₹875.54 |
| Profit Margin | 8.44% |

**Calculation methodology:**

- Average Order Value = Total Sales / Unique Orders
- Profit Margin = Total Profit / Total Sales × 100

**Reporting Note:** The dashboard PDF contains a Q1-filtered screenshot. The full-year metrics above are calculated separately from the complete CSV datasets and should not be confused with the filtered dashboard figures.

---

## 3. Key Diagnostic Insights

### Insight 1: Revenue Leaders Are Not Necessarily the Highest Profit Contributors

| Category | Sales | Sales Share | Profit | Profit Margin | Units |
|---|---:|---:|---:|---:|---:|
| Electronics | ₹166,267 | 37.98% | ₹13,162 | 7.92% | 1,154 |
| Clothing | ₹144,323 | 32.97% | ₹13,325 | 9.23% | 3,516 |
| Furniture | ₹127,181 | 29.05% | ₹10,476 | 8.24% | 945 |

**Commercial Insight:**

Electronics generated the highest sales, contributing 37.98% of total revenue.

However, Clothing generated the highest profit of ₹13,325 and achieved a higher profit margin of 9.23%, compared with Electronics at 7.92%.

Clothing also recorded the highest unit volume, with 3,516 units sold.

**Business Implication:**

Revenue contribution alone should not determine promotional investment. Product-category decisions should also consider profitability and sales volume.

### Insight 2: Five Sub-Categories Recorded Combined Losses of ₹2,296

Printers emerged as the highest-profit sub-category, generating ₹8,606, equivalent to approximately 23.28% of total recorded profit.

However, five sub-categories recorded negative profit:

| Sub-Category | Recorded Profit |
|---|---:|
| Furnishings | -₹806 |
| Electronic Games | -₹644 |
| Kurti | -₹401 |
| Skirt | -₹315 |
| Leggings | -₹130 |
| **Combined Loss** | **-₹2,296** |

**Commercial Insight:**

These five sub-categories represent an important area for profitability investigation.

If their recorded losses were eliminated while all other results remained unchanged, total profit would increase by ₹2,296, equivalent to approximately 6.21% of the current profit baseline.

**Business Implication:**

Further investigation should examine product costs, supplier pricing, discounting and return-related expenses before making pricing or product assortment decisions.

*Note: The 6.21% figure is a mathematical scenario, not a guaranteed profit improvement.*

### Insight 3: High Geographic Revenue Concentration

The five highest-sales states were:

| State | Sales |
|---|---:|
| Maharashtra | ₹102,498 |
| Madhya Pradesh | ₹87,463 |
| Uttar Pradesh | ₹38,362 |
| Delhi | ₹22,957 |
| Rajasthan | ₹22,334 |

Maharashtra and Madhya Pradesh together contributed **43.39% of total sales**.

The top five states accounted for approximately **62.50% of total sales**.

**Commercial Insight:**

A significant proportion of sales originated from two states, highlighting the importance of monitoring geographic revenue concentration.

**Business Implication:**

Further regional analysis could compare customer acquisition, order volume, profitability and fulfilment performance across states before defining expansion priorities.

### Insight 4: Monthly Profitability Fluctuations & Payment Behaviour

**Monthly Profitability**

- November recorded the highest monthly profit: ₹10,253.
- May recorded the largest monthly loss: -₹3,730.
- July, September and December also recorded negative monthly profit.

**Payment Behaviour**

| Payment Mode | Units | Share of Units |
|---|---:|---:|
| COD | 2,456 | 43.74% |
| UPI | 1,157 | 20.61% |
| Debit Card | 741 | 13.20% |
| Credit Card | 672 | 11.97% |
| EMI | 589 | 10.49% |

**Commercial Insight:**

COD represented the largest share of total units sold, accounting for 43.74%.

November demonstrated the strongest monthly profitability, while May recorded the weakest result.

**Business Implication:**

The business could investigate monthly discounting, product mix and cost patterns to understand profitability fluctuations. Payment analysis could also be extended by integrating failed deliveries, returns and payment settlement information.

---

## 4. Strategic Action Plan

| Strategic Priority | Recommended Business Action | Measurement Focus |
|---|---|---|
| Profitability Recovery | Investigate the five loss-making sub-categories through product cost, pricing, discount and return analysis. | Sub-category profit and SKU-level margins |
| Product Mix Optimisation | Compare category-level profitability before changing promotional allocation. | Sales contribution, profit and unit volume |
| Monthly Performance Control | Investigate May's negative profit and review monthly promotional and product-mix performance. | Monthly profit and profit margin |
| Payment Behaviour Analysis | Evaluate COD and digital payment performance using transaction and delivery data. | Payment distribution, failed deliveries and settlement time |
| Regional Performance | Compare state-level sales, profitability and order volume to identify opportunities for further analysis. | State-level revenue, profit and orders |

The action plan identifies areas for business investigation. Financial improvements cannot be quantified reliably without additional operational and cost data.

---

## 5. Dashboard & Project Deliverables

The project includes:

- **Orders.csv:** Order-level customer, date and geographic information.
- **Details.csv:** Transaction-level sales, profit, quantity, category and payment information.
- **FIRST dashbard.pdf:** PDF preview of the Power BI dashboard.

The dashboard provides interactive business views covering:

- Profit by month.
- Sales by state.
- Quantity by product category.
- Sales by customer.
- Quantity by payment mode.
- Profit by sub-category.

The supplied PDF screenshot has the Q1 filter selected. Its figures represent a filtered dashboard view rather than the full-year baseline.

---

## 6. Scope, Limitations & Phase 2 Roadmap

### Scope and Limitations

This analysis is based on FY 2018 order and transaction records supplied in Orders.csv and Details.csv.

The available datasets do not contain:

- SKU-level cost of goods sold.
- Supplier pricing.
- Discount and promotion history.
- Marketing expenditure or customer acquisition cost.
- Returns, cancellations and failed deliveries.
- Return-to-Origin (RTO) expenses.
- Payment settlement timelines.

Therefore, the analysis identifies commercial patterns and potential areas for investigation rather than establishing the root causes of profitability changes.

### Phase 2 Roadmap

Future analysis could be strengthened by integrating:

1. Product-level cost and supplier datasets.
2. Discount and promotional campaign records.
3. Return, cancellation and delivery information.
4. Marketing expenditure and customer acquisition data.
5. Payment settlement and transaction-cost information.

These additional datasets would support deeper profitability diagnostics, root-cause analysis and more comprehensive business performance reporting.

---

## 7. Tools & Skills Demonstrated

**Tools**
- Microsoft Power BI
- DAX
- CSV datasets

**Analytical Skills**
- Data validation and quality checks.
- Relational data modelling.
- KPI calculation.
- Sales and profitability analysis.
- Category and sub-category performance analysis.
- Regional sales analysis.
- Monthly trend analysis.
- Payment behaviour analysis.
- Business insight development.
- Data storytelling and dashboard reporting.

---

## Author

**Bhumika Chauhan**

LinkedIn: https://www.linkedin.com/in/bhumika-chauhan-342a0b36b/

*E-Commerce Commercial Performance & Profitability Diagnostics — FY 2026*
