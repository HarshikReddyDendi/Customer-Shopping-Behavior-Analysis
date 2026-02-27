# Customer-Shopping-Behavior-Analysis
This project represents a complete, industry standard, end-to-end data analytics workflow, designed to mirror the real responsibilities of professional analysts in modern business environments. The project encompasses all critical stages of data analysis, from data preparation and modeling to insight generation, visualization, and reporting

# Customer Shopping Behavior Analysis

## 📋 Project Overview

This project analyzes customer shopping behavior using transactional data from 3,900 purchases across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

## 📊 Dataset Summary

- **Total Records:** 3,900 transactions
- **Features:** 18 columns
- **Missing Data:** 37 values in Review Rating column (handled via median imputation)

### Key Features

**Customer Demographics:**
- Age, Gender, Location, Subscription Status

**Purchase Details:**
- Item Purchased, Category, Purchase Amount, Season, Size, Color

**Shopping Behavior:**
- Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

## 🛠️ Technologies Used

- **Python** - Data cleaning, EDA, and database integration (pandas, numpy)
- **PostgreSQL** - SQL analysis and business queries
- **Power BI** - Interactive dashboard visualization
- **Jupyter Notebook** - Analysis documentation

## 📈 Analysis Workflow

### 1. Data Preparation (Python)
- Imported and explored dataset structure
- Handled missing values using category-based median imputation
- Standardized column names to snake_case
- Verified data consistency and redundancies

### 2. Feature Engineering
- Created `age_group` column by binning customer ages
- Created `purchase_frequency_days` from purchase data
- Identified and removed redundant columns

### 3. SQL Analysis
Conducted 10 key business analyses using PostgreSQL:

| Analysis | Key Finding |
|----------|-------------|
| Revenue by Gender | Female: $75,191 | Male: $157,890 |
| High-Spending Discount Users | 839 customers used discounts but spent above average |
| Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Skirt (3.78) |
| Shipping Type Comparison | Express ($60.48) > Standard ($58.46) |
| Subscribers vs. Non-Subscribers | Subscribers: 1,053 (avg $59.49), Non-Subscribers: 2,847 (avg $59.87) |
| Discount-Dependent Products | Hat (50%), Sneakers (49.66%), Coat (49.07%), Sweater (48.17%), Pants (47.37%) |
| Customer Segmentation | Loyal: 3,116 | Returning: 701 | New: 83 |
| Top 3 Products/Category | Jewelry, Sunglasses, Belt (Accessories); Blouse, Pants, Shirt (Clothing) |
| Repeat Buyers & Subscriptions | 958 repeat buyers with subscriptions vs. 2,518 without |
| Revenue by Age Group | Young Adult: $62,143 | Middle-aged: $59,197 | Adult: $55,978 | Senior: $55,763 |

### 4. Visualization (Power BI)
Interactive dashboard with:
- Customer count and average purchase metrics
- Subscription status distribution (27% subscribed)
- Revenue and sales by category, age group, and shipping type
- Filterable views by multiple dimensions

## 📁 Project Structure

```
customer-shopping-analysis/
├── README.md
├── data/
│   └── customer_shopping_behavior.csv
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   └── 03_analysis.ipynb
├── sql/
│   └── business_queries.sql
├── dashboards/
│   └── customer_behavior_dashboard.pbix
└── docs/
    └── analysis_report.pdf
```

## 🎯 Key Business Insights

1. **Gender Disparity:** Male customers generate significantly more revenue ($157,890) compared to females ($75,191)

2. **Subscription Opportunity:** Despite 73% non-subscription rate, subscribers maintain comparable average spending ($59.49 vs $59.87)

3. **Express Shipping Premium:** Customers choosing express shipping spend slightly more ($60.48) than standard ($58.46)

4. **Loyal Customer Base:** 79.9% of customers are in the "Loyal" segment, indicating strong retention potential

5. **Product Quality vs. Discounts:** Gloves and Sandals have highest ratings (3.86, 3.84) despite moderate discount dependency

6. **Age-Based Revenue:** Young adults contribute the most revenue ($62,143), suggesting a younger customer demographic

## 💡 Business Recommendations

### 1. Boost Subscriptions
- Promote exclusive benefits for subscribers (early access, special discounts)
- Target non-subscribers with incentive campaigns
- Potential revenue impact: 1,794 non-subscriber accounts × avg spending = $107,000+

### 2. Customer Loyalty Programs
- Reward repeat buyers to move them from "Returning" to "Loyal" segment
- Focus on 701 returning customers with personalized offers
- Potential to increase loyalty segment by 20-30%

### 3. Review Discount Policy
- Balance sales boosts (50% Hat discount rate) with margin control
- Limit discounts on high-rated products (Gloves, Sandals)
- Maintain discounts on lower-rated items to drive sales

### 4. Product Positioning
- Highlight top-rated products (Gloves, Sandals, Boots) in marketing campaigns
- Feature best-sellers from each category in promotional materials
- Cross-sell complementary products

### 5. Targeted Marketing
- Prioritize young adult age group for new product launches (highest revenue contributor)
- Create express shipping promotions (higher spending segment)
- Develop gender-specific campaigns to close revenue gap

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy psycopg2 jupyter matplotlib seaborn
```

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/customer-shopping-analysis.git
   cd customer-shopping-analysis
   ```

2. **Load data:**
   ```python
   import pandas as pd
   df = pd.read_csv('data/customer_shopping_behavior.csv')
   ```

3. **Run analysis:**
   ```bash
   jupyter notebook notebooks/01_data_cleaning.ipynb
   ```

4. **Database Setup (PostgreSQL):**
   ```bash
   psql -U postgres -d your_database -f sql/business_queries.sql
   ```

## 📊 Dashboard Access

Open the Power BI dashboard file (`customer_behavior_dashboard.pbix`) to explore:
- Real-time KPI metrics
- Interactive filters by demographics and purchase behavior
- Drill-down capabilities across categories and time periods

## 📝 Data Cleaning Steps

- Handled 37 missing Review Rating values using median imputation by product category
- Verified discount_applied and promo_code_used for redundancy
- Standardized all column naming conventions
- Validated data types and ranges

## 🔍 SQL Queries

All business queries are documented in `sql/business_queries.sql` with comments explaining:
- Query purpose
- Expected output format
- Business interpretation

## 📚 Documentation

Detailed analysis methodology and findings are documented in `docs/analysis_report.pdf`

## 💬 Key Metrics

| Metric | Value |
|--------|-------|
| Total Revenue | $233,081 |
| Average Purchase Amount | $59.76 |
| Average Review Rating | 3.75 |
| Subscription Rate | 27% |
| Repeat Buyer Rate | 25.2% |

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -am 'Add analysis insights'`)
4. Push to branch (`git push origin feature/improvement`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see LICENSE file for details

## 👤 Author

[Your Name/Organization]

## 📧 Contact & Questions

For questions or suggestions about this analysis, please open an issue or contact the project maintainers.

---

**Last Updated:** February 2026  
**Dataset Version:** 1.0  
**Analysis Status:** Complete ✅
