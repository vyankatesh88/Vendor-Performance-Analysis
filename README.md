
# 🧾 Vendor Performance Analysis – Retail Inventory & Sales

_Analyzing vendor efficiency and profitability to support better purchasing and inventory strategies using SQL, Python, and Power BI._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project evaluates vendor performance and inventory patterns in the retail sector to generate actionable insights for decision-making. A full pipeline was built where SQL was used for data extraction and transformation, Python for cleaning, analysis, and hypothesis testing, and Power BI for creating interactive dashboards.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>
Retail businesses often face challenges with:

- Identifying underperforming brands needing promotions or pricing changes
- Understanding vendor contributions to overall sales and profit
- Assessing the cost–benefit of bulk purchases
- Detecting slow-moving or unsold inventory
- Comparing profitability across different vendors

This project addresses these challenges with data-driven analysis.

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Multiple CSV files containing sales, vendor, and inventory information
- Data was ingested into SQL, cleaned, and transformed into summary tables for further analysis

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- SQL (Common Table Expressions, Joins, Filtering)
- Python (Pandas, Matplotlib, Seaborn, SciPy)
- Power BI (Interactive Visualizations)
- GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
vendor-performance-analysis/
│
├── README.md
├── .gitignore
├── requirements.txt
├── Vendor Performance Report.pdf
│
├── notebooks/                  # Jupyter notebooks
│   ├── exploratory_data_analysis.ipynb
│   ├── vendor_performance_analysis.ipynb
│
├── scripts/                    # Python scripts for ingestion and processing
│   ├── ingestion_db.py
│   └── get_vendor_summary.py
│
```

---
<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

- Removed transactions with:
  - Gross Profit ≤ 0
  - Profit Margin ≤ 0
  - Sales Quantity = 0
- Created summary tables with vendor-level metrics
- Converted data types, handled outliers, merged lookup tables

---
<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

**Negative or Zero Values Detected:**
- Gross Profit: Min -52,002.78 (loss-making sales)
- Profit Margin: Min -∞ (sales at zero or below cost)
- Unsold Inventory: Indicating slow-moving stock

**Outliers Identified:**
- High Freight Costs (up to 257K)
- Large Purchase/Actual Prices

**Correlation Analysis:**
- Weak between Purchase Price & Profit
- Strong between Purchase Qty & Sales Qty (0.999)
- Negative between Profit Margin & Sales Price (-0.179)

---
<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Brands for Promotions**: 198 brands with low sales but high profit margins
2. **Top Vendors**: Top 10 vendors = 65.69% of purchases → risk of over-reliance
3. **Bulk Purchasing Impact**: 72% cost savings per unit in large orders
4. **Inventory Turnover**: $2.71M worth of unsold inventory
5. **Vendor Profitability**:
   - High Vendors: Mean Margin = 31.17%
   - Low Vendors: Mean Margin = 41.55%
6. **Hypothesis Testing**: Statistically significant difference in profit margins → distinct vendor strategies

---


---
<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the repository:
```bash
git clone https://github.com/yourusername/vendor-performance-analysis.git
```
3. Load the CSVs and ingest into database:
```bash
python scripts/ingestion_db.py
```
4. Create vendor summary table:
```bash
python scripts/get_vendor_summary.py
```
5. Open and run notebooks:
   - `notebooks/exploratory_data_analysis.ipynb`
   - `notebooks/vendor_performance_analysis.ipynb`

---
<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Diversify vendor base to reduce risk
- Optimize bulk order strategies
- Reprice slow-moving, high-margin brands
- Clear unsold inventory strategically
- Improve marketing for underperforming vendors

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Ayushi Mishra**  
Data Analyst  
📧 Email: vyankateshpanchal04@gmail.com 
🔗 [LinkedIn](https://www.linkedin.com/in/vyankatesh-panchal/) 
