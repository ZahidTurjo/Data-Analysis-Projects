## Zomato Restaurants in India - Exploratory Data Analysis

This project performs a detailed Exploratory Data Analysis (EDA) of the Zomato Restaurants dataset. It covers data cleaning, transformation, and visualization to uncover meaningful insights about restaurants, cities, cuisines, price range, establishment types, and customer preferences across the country.

## 📦 Libraries Used

- **NumPy**: Efficient mathematical computations on arrays.
- **Pandas**: Handling structured data using DataFrames.
- **Matplotlib**: Customizable plotting for visualization.
- **Seaborn**: Simplified statistical data visualization.
- **Warnings**: To suppress unnecessary alerts during analysis.

---

## 📌 Dataset Overview

- 📊 **Total Rows**: 211,944 → Cleaned to **55,568 unique restaurants**
- 🔢 **Columns**: 26 → Includes restaurant name, city, price range, cuisine, ratings, etc.

---

## 🧹 Data Cleaning Steps

- Removed duplicates based on `res_id`.
- Set `res_id` as the index.
- Fixed malformed `establishment` column and replaced empty entries with `Other establishments`.
- Handled missing values:
  - `zipcode`: Filled with `"Others"`
  - `cuisines`, `timings`: Reviewed, not dropped
- Standardized categorical columns like `currency`, `delivery`, `takeaway`.

---

## 🔍 Exploratory Data Analysis (EDA)

### 🏙️ Top & Bottom Cities by Restaurant Count

- **Top Cities**: Bangalore, Mumbai, Pune, Chennai, and New Delhi dominate.
- **Bottom Cities**: Faridabad, Nasik, Ghaziabad, etc., have fewer listings.

### 🍕 Top Restaurant Chains

- Most outlets: Domino's Pizza, Café Coffee Day, KFC, Baskin Robbins
- Consumer preferences lean heavily toward pizza, burgers, and chicken.

### 🏪 Establishment Types

- Dominant: Quick Bites, Casual Dining
- Least common: Mess, Butcher Shop, Irani Café

### 🍱 Popular Cuisines

- North Indian cuisine is most served.
- Others: Fast Food, Chinese, South Indian, and Bakery

### 💸 Price Range Analysis

| Category | Price Range (INR) | Description         |
|----------|-------------------|---------------------|
| 1        | 50–450            | Inexpensive         |
| 2        | 250–999           | Moderate            |
| 3        | 500–1900          | Expensive           |
| 4        | 1000–30000        | Very Expensive      |

- Most restaurants fall into **Category 1**
- KDE Plot shows the average cost for two is most dense around 500–600 INR.

### 🌟 Ratings Distribution

- Majority of ratings are between 3 and 4.
- Some restaurants have no ratings (likely new/unreviewed).
- Restaurants in lower price ranges often have **higher ratings**.

### 🛍️ Service Availability

| Service Type          | Percentage |
|-----------------------|------------|
| Takeaway Available    | 44.6%      |
| Delivery Available    | 43.0%      |
| No Delivery Available | 12.4%      |

### 💰 Top 10 Most Expensive Restaurants

| Name                                   | City       | Type         | Cost for Two |
|----------------------------------------|------------|--------------|--------------|
| Ocean - Sahara Star                    | Mumbai     | Fine Dining  | ₹30,000      |
| Gol Bungalow - Taj Falaknuma          | Hyderabad  | Fine Dining  | ₹15,000      |
| Bhairo                                | Udaipur    | Fine Dining  | ₹15,000      |
| Fly Dining                             | Bangalore  | Fine Dining  | ₹14,000      |
| Trophy Bar – Umaid Bhawan              | Jodhpur    | Bar          | ₹12,000      |
| ...                                    | ...        | ...          | ...          |

---

## 📈 Visuals & Insights

- Bar plots of top cities, establishments, cuisines
- Pie charts for service availability
- KDE plot for average price density
- Box plot showing price vs rating relationship

---

## 🧠 Key Takeaways

- Consumers prefer affordable options (Category 1)
- North Indian cuisine dominates across cities
- Quick Bites and Casual Dining are the most common types
- Lower-priced restaurants tend to receive better ratings
- Big chains like Domino's and KFC dominate presence

---

## 🛠️ Future Improvements

- Add interactive dashboards ( Power BI)
- Use NLP on reviews to assess sentiment
- Cluster cities/restaurants using unsupervised learning

---

## 📌 Conclusion

This EDA provides a comprehensive view of India’s restaurant landscape using Zomato data. It uncovers deep insights into consumer behavior, pricing, and service offerings that could inform restaurant businesses or food tech startups.

---

