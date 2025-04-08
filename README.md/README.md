# Quantium Virtual Internship – Retail Strategy and Analytics

This repository contains my work for the Quantium Virtual Internship, focusing on retail analytics. The goal is to analyze customer transactions and purchasing behavior, clean and visualize the data, and draw actionable insights to support business decisions.

---

## Project Structure

```
quantium-internship/
├── data/                         # Raw datasets
│   ├── QVI_transaction_data.xlsx
│   └── QVI_purchase_behaviour.csv
├── step1/                        # Step 1: Data Cleaning & EDA
│   ├── step1.ipynb      
├── README.md                     # Project overview and documentation
```

---

## Technologies Used

- Python (Pandas, NumPy)
- Matplotlib, Seaborn
- Jupyter Notebook
- Git & GitHub

---

## Step 1 – Data Cleaning & EDA

### Key Tasks

- Merged transaction and customer data using `LYLTY_CARD_NBR`
- Removed irrelevant records (e.g. magazines, mislabelled salsa items)
- Standardized brand names with SQL-style mapping
- Extracted `PACK_SIZE` from product names using regex
- Identified and removed outliers from `TOT_SALES` and `PROD_QTY`
- Conducted and visualized:
  - Top-selling products
  - Sales by lifestage and premium status
  - Average quantity and unit price per customer group

---

## Exploratory Data Analysis

This section summarizes the initial findings on product performance and customer behavior using various groupings and metrics.

### Top-Selling Products

By aggregating total sales, the top 10 highest-selling product IDs were identified as:

4, 14, 16, 102, 7, 23, 20, 89, 32, 88

These are likely to be popular items with high repeat purchase potential.

---

### Sales by Customer Segments

#### By Lifestage

- OLDER SINGLES/COUPLES had the highest sales (~350,000 AUD)
- NEW FAMILIES had the lowest (~50,000 AUD)

#### By Premium Tier

- Mainstream customers made up the largest portion of sales (~650,000 AUD)
- Premium customers generated the least (~420,000 AUD)

This suggests that older and mainstream groups are the core revenue drivers.

---

### Average Units Purchased per Customer Segment

By grouping `LIFESTAGE` with `PREMIUM_CUSTOMER`, we observed:

- Older Families and Young Families bought more units per customer.
- Young Singles/Couples tended to buy fewer units across all tiers.

This indicates families are more frequent or higher-volume buyers.

---

### Average Purchase Price per Segment

We also examined the average purchase price per customer group (total sales divided by total quantity):

- Young Singles/Couples – Mainstream had the highest average price (> 4.1 AUD)
- New Families – Budget had the lowest (~3.97 AUD)
- Retirees – Premium also showed relatively high prices (~3.95 AUD)

#### Key Takeaways

- Lifestage influences price sensitivity more than premium tier.
- Young mainstream customers are willing to pay more, likely due to brand or lifestyle preferences.
- Budget-conscious family groups may respond well to promotions.
- Retirees consistently show interest in premium options.

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/qiuqiu035/quantium-internship
```
2. Open `step1/step1.ipynb` using Jupyter Notebook
3. Run all cells to replicate the analysis and visualizations

---

## Author

Maintained by qiuqiu035.  
Feel free to fork, explore, or contribute.
