# elevate-labs-task01-amazon-data
# 🛒 Amazon Product Sales Data Preprocessing – Elevate Labs Task 01

This repository contains the preprocessing work done for Task 01 of the Elevate Labs Internship using the [Amazon Sales Dataset](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset). The dataset includes product details, pricing, ratings, reviews, and links.

---

## 📁 Dataset Overview

- Source: Kaggle
- Title: Amazon Sales Dataset
- Columns include:
  - `product_id`, `product_name`, `category`
  - `discounted_price`, `actual_price`, `discount_percentage`
  - `rating`, `rating_count`
  - `about_product`, `user_id`, `user_name`, `review_id`, `review_title`, `review_content`
  - `img_link`, `product_link`

---

## 🔧 Preprocessing Summary

The following preprocessing steps were applied using Python and Pandas:

1. **Column Renaming**  
   Standardized all column names to lowercase with underscores (`_`) instead of spaces.

2. **Price Cleanup**  
   - Removed symbols like ₹ and commas from `discounted_price` and `actual_price`.
   - Converted both to numeric types (int/float).

3. **Discount and Rating Conversion**  
   - Removed `%` from `discount_percentage` and converted to numeric.
   - Converted `rating` and `rating_count` to numeric values.

4. **Text Cleaning**
   - Cleaned `about_product` by replacing `|` with sentence separators.
   - Converted text to lowercase and removed special characters.

5. **Splitting Multi-Value Columns**
   - Split comma-separated fields like `user_id`, `user_name`, `review_id`, etc., into lists.
   - Calculated `num_reviews` per product.

6. **Missing Value Handling**
   - Filled missing numeric fields with 0 for consistency.

7. **Export**
   - Final cleaned dataset was exported to Excel as `cleaned_products.xlsx`.

---

## 💻 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/elevate-labs-task01.git
   cd elevate-labs-task01
2. Install required libraries:
   pip install pandas openpyxl
3. Run the preprocessing script:
   python preprocess.py

Use Cases of This Cleaned Dataset
Sentiment analysis on product reviews

Product recommendation systems

Price vs rating correlation studies

Review-based product ranking

👤 Author
Rachna Verma
M.Sc. Data Science | CHRIST (Deemed to be University)
📧 Email: rv124936@gmail.com
