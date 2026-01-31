# Food Delivery Data Analysis 🍔📊

## Project Overview
This project involves analyzing a real-world dataset from a food delivery platform. The goal is to clean, merge, and analyze data from three distinct file formats (**CSV, JSON, SQL**) to derive actionable business insights regarding user behavior, restaurant performance, and revenue trends.

## 📂 Datasets Used
The analysis combines data from three different sources:

1.  **`orders.csv`** (Transactional Data):
    * Contains 10,000 order records.
    * *Columns:* `order_id`, `user_id`, `restaurant_id`, `order_date`, `total_amount`.
2.  **`users.json`** (User Master Data):
    * Contains 3,000 user profiles.
    * *Columns:* `user_id`, `name`, `city`, `membership` (Gold/Regular).
3.  **`restaurants.sql`** (Restaurant Master Data):
    * Contains 500 restaurant details (extracted from SQL INSERT statements).
    * *Columns:* `restaurant_id`, `restaurant_name`, `cuisine`, `rating`.

## 🛠️ Tech Stack
* **Language:** Python 🐍
* **Libraries:**
    * `pandas` (Data Manipulation & Aggregation)
    * `re` (Regular Expressions for parsing SQL)
    * `ast` (Safe evaluation of string literals)
* **Environment:** Jupyter Notebook

## ⚙️ Methodology
1.  **Data Loading:**
    * Loaded transactional data from CSV.
    * Loaded user data from JSON.
    * Parsed raw SQL `INSERT` statements using Python's string manipulation and regex to extract restaurant data into a DataFrame.
2.  **Data Merging:**
    * Performed a **Left Join** between Orders and Users on `user_id`.
    * Performed a **Left Join** between the result and Restaurants on `restaurant_id`.
3.  **Data Analysis:**
    * Analyzed revenue distribution by city and membership type.
    * Evaluated cuisine popularity and average order values.
    * Identified high-performing restaurants based on ratings and order volume.

## 📊 Key Insights Derived
* **Customer Segmentation:** Analysis of spending habits between **Gold** vs. **Regular** members.
* **Regional Performance:** Identified top-performing cities (e.g., Chennai, Hyderabad) based on total revenue.
* **Cuisine Trends:** Determined which cuisines (e.g., Italian, Mexican) drive the highest average order values.
* **Restaurant Ratings:** Correlated restaurant ratings with total order revenue.

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/YOUR-USERNAME/Food-Delivery-Data-Analysis.git](https://github.com/YOUR-USERNAME/Food-Delivery-Data-Analysis.git)
    ```
2.  Install required libraries:
    ```bash
    pip install pandas
    ```
3.  Open the Jupyter Notebook:
    ```bash
    jupyter notebook Food_Delivery_Analysis.ipynb
    ```
4.  Run all cells to see the data processing and analysis results.

## 📝 Author
* **Pavankumar S**
* *Submitted for the Data Analysis Hackathon*
