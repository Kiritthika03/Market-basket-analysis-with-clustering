# 🛍️ Customer Segmentation and Market Basket Analysis

This project explores customer purchasing behavior using **RFM Analysis** and **Market Basket Analysis (MBA)** on the `Online Retail II` dataset. The goal is to segment customers based on their transaction patterns and identify product combinations that are frequently bought together.

---

## 📁 Dataset
- **Name:** Online Retail II Dataset  
- **Source:** [UCI / Kaggle](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II)  
- **Format:** CSV  
- **Fields:** Invoice, StockCode, Description, Quantity, InvoiceDate, UnitPrice, Customer ID, Country

---

## 🔍 Project Objectives

1. **RFM (Recency, Frequency, Monetary) Analysis**
   - Segment customers based on their purchase history.
   - Rank customers using normalized RFM scores.
   - Apply **KMeans clustering** for automated segment discovery.

2. **Market Basket Analysis (MBA)**
   - Generate association rules using the **FPGrowth** algorithm.
   - Identify product pairs frequently bought together.
   - Use **lift** and **confidence** to evaluate the strength of rules.

---

## 📊 Techniques Used

- **Pandas & NumPy** for data preprocessing
- **RFM Feature Engineering**
- **Ranking-based Normalization**
- **KMeans Clustering**
- **FPGrowth Algorithm (mlxtend)**
- **Association Rule Mining**
- **Matplotlib / Seaborn** for visualization

---

## 📈 Key Insights

### RFM Analysis:
- Customers with high Frequency and low Recency were clustered as **Champions**.
- RFM-based segmentation revealed distinct behaviors such as:
  - **Loyal** repeat buyers
  - **At-risk** customers
  - **Low-value churned** segments

### Market Basket Analysis:
- Popular product pairs:
  - `"WHITE HANGING HEART T-LIGHT HOLDER"` → `"STRAWBERRY CERAMIC TRINKET BOX"` (Lift: 1.65)
  - `"ASSORTED COLOUR BIRD ORNAMENT"` → `"HOME BUILDING BLOCK WORD"` (Lift: 2.33)
- Products with high **lift** indicate strong potential for **cross-selling**.

---

## 🛠 How to Run

```bash
# Install dependencies
pip install pandas matplotlib seaborn scikit-learn mlxtend

# Run notebook or script
jupyter notebook RFM_MBA_Analysis.ipynb
