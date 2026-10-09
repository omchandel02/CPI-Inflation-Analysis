# India CPI Inflation Analysis
### Basket Contribution · Y-o-Y Trend · Food Inflation · COVID-19 Impact · Crude Oil Correlation

An **Excel-based** case study on India's Consumer Price Index (CPI), analyzing how inflation is distributed across the consumer basket and what drove it between 2013 and 2023. Framed as an analyst at the National Statistical Office answering five stakeholder questions, using rural, urban and combined (rural + urban) CPI index data.

## What's included

| File | Purpose |
|---|---|
| `CPI_Inflation_Analysis1.xlsx` | Full workbook: cleaned data, five analysis sheets (with charts), and supporting data tabs |
| `CPI_Inflation_Problem_Statement.pdf` | Case study brief and the five questions answered |

## Dataset overview

- **Source:** CPI index data from the Government of India website
- **Coverage:** January 2013 to May 2023, across 3 sectors (Rural, Urban, Rural+Urban), 375 sector-month records
- **Fields:** 26 category indices (cereals, meat and fish, vegetables, housing, fuel and light, health, education, transport and communication, etc.) plus the General Index
- **Supporting data:** a monthly imported crude oil price series (January 2021 to May 2023, 29 months)

> CPI values are an index, not a price level, so values are never summed across months. Percentage changes are used for all trend work.

## Business questions answered

1. Which broader category contributes most to the CPI basket (latest month)?
2. What is the Y-o-Y inflation trend since 2017, and which year was highest?
3. What drove food inflation over the 12 months ending May 2023?
4. How did the onset of COVID-19 (March 2020) affect inflation across categories?
5. How strongly do imported crude oil prices move with category-level inflation?

## Approach

- **Data cleaning:** the raw extract had 240+ missing or `NA` cells; gaps were filled using **moving-average imputation**
- **Bucketing:** 26 granular categories grouped into broader buckets: Food (Veg / Non-veg), Luxury, Clothing, Housing, Transportation, Health, Education, Miscellaneous
- **Contribution analysis:** each bucket's share of the basket in May 2023, so shares add to 100%
- **Growth rates:** Y-o-Y and M-o-M % change calculated from index values, per the case study formulas
- **Correlation:** Excel's `CORREL` between monthly crude oil prices and each category's index

## Key findings

**1. Basket contribution (May 2023):** Food is the largest block at about **46%** of the basket (Food-Veg 37.5% + Non-veg 8.3%), far ahead of Luxury (15.7%), Clothing (11.9%), and Housing and Transportation (7.5% each).

**2. Y-o-Y inflation (May on May):** **2022 was the peak at 7.04%**, followed by 2020 (6.35%) and 2021 (6.21%); 2019 was the low at 3.05%. The 2022 spike is consistent with the Russia-Ukraine war pushing up global commodity, fuel and edible oil prices.

**3. Food inflation, May 2022 to May 2023:**
- Food index rose **3.0%** over the 12 months
- Highest M-o-M rise: **June 2022 (+1.07%)**; lowest: **February 2023 (-0.68%)**
- Biggest individual contributor: **Spices, +17.9% Y-o-Y** (index 184.9 to 218.0), followed by **Cereals, +12.7%**
- Biggest drag: **Oils and fats, -16.0%**, then Vegetables (-7.9%)

**4. COVID-19 impact (Rural+Urban, March-to-March Y-o-Y):**

| Category | 2019-20 (pre-lockdown) | 2020-21 (post-lockdown) |
|---|---|---|
| Food | 7.9% | 7.1% |
| Clothing | 1.9% | 4.3% |
| Housing | 2.8% | 3.4% |
| Health | 4.2% | 6.2% |

Health and clothing inflation accelerated after the first lockdown, while food inflation was already elevated going in and eased slightly.

**5. Crude oil correlation (Jan 2021 to May 2023):** crude oil rose about **127%** from January 2021 to its April 2022 peak, then fell about 32% by May 2023. The strongest relationships were **Meat and fish (0.79)**, **Transport and communication (0.78)**, **Oils and fats (0.75)** and **Recreation (0.72)**; the General Index correlated at 0.70, and Egg showed essentially none (-0.08).

## Limitations

- Correlation does not imply causation; a shared upward trend over 2021 to 2023 can inflate coefficients.
- Equal weights are used across categories, as the case study specifies; official CPI uses expenditure-based weights, so these contributions are illustrative.
- The source data includes aggregate rows (such as "Food and beverages" and "Clothing and footwear") alongside their components. Excluding them, Food's share is 45.6%, so the ranking of categories is unchanged.
- Rural housing is not published in the source data, so Housing reflects urban values only.

## Tools & skills demonstrated

Excel (formulas, `CORREL`, pivot-style summaries, charts) · Data cleaning and moving-average imputation · Index and percentage-change analysis · Exploratory data analysis · Data storytelling

## How to use

1. Download `CPI_Inflation_Analysis1.xlsx` and open it in Excel.
2. Review the sheets `Analysis1` to `Analysis5`, one per business question; each has its supporting data tab.

---

**Connect with me:** [LinkedIn](https://www.linkedin.com/in/om-chandel/)
