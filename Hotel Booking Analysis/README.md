# Hotel Booking Analysis:

## Project Overview
This project involves analyzing a dataset of hotel bookings to understand various factors influencing booking patterns, cancellations, customer preferences, and revenue generation. The goal is to provide actionable insights and recommendations to stakeholders for improving business strategies.

## [Colab Notebook Link](https://colab.research.google.com/drive/1gBkAoNSnOmJjvekvvbkC2Rx8YxFMofvo?usp=sharing)

## Data Overview
The dataset contains detailed information about hotel bookings, including arrival dates, lead times, guest demographics, booking changes, and cancellation status. Initial data inspection revealed:
- The dataset contains 119,390 entries and 32 columns.
- Columns like `children`, `country`, `agent`, and `company` had missing values.
- There were 31,994 duplicate entries.

### Data Cleaning and Wrangling Steps:
1.  **Duplicate Removal**: Duplicated rows were removed, reducing the dataset to 87,396 unique entries.
2.  **Missing Value Imputation**:
    -   `children` nulls were filled with `0` (assuming no children).
    -   `country` nulls were filled with `'Others'`.
    -   `agent` and `company` nulls were filled with `0` (assuming no agent/company involved).
3.  **Invalid Entries**: Rows where `adults`, `children`, and `babies` summed to zero (indicating no guests) were removed.
4.  **Feature Engineering**:
    -   `total_people`: Sum of `adults`, `children`, and `babies`.
    -   `total_stay`: Sum of `stays_in_weekend_nights` and `stays_in_week_nights`.

## Exploratory Data Analysis (EDA) - Key Findings

### 1. Hotel Type Preference
-   **City Hotels** are significantly more preferred by guests than Resort Hotels, accounting for a larger share of bookings.

### 2. Booking Cancellation Trends
-   Approximately **27.5%** of bookings are canceled.
-   **City Hotels** have a higher cancellation rate (30.1%) compared to Resort Hotels (23.5%).

### 3. Guest Preferences
-   **Meal Type**: **BB (Bed and Breakfast)** is the most preferred meal type.
-   **Arrival Year**: **2016** saw the most bookings, with a noticeable drop in 2017.
-   **Arrival Month**: **August and July** are the busiest months for bookings.
-   **Country of Origin**: Most guests originate from **PRT (Portugal)**.
-   **Distribution Channel**: **TA/TO (Travel Agents/Tour Operators)** is the most used distribution channel.
-   **Room Type**: Room type **'A'** is the most preferred by guests, however, there's a discrepancy between preferred and assigned room types, which could be a reason for cancellations.
-   **Agents**: Agent **ID 9** made the most bookings.
-   **Repeated Guests**: Only about **3.86%** of guests are repeated, indicating low guest loyalty.
-   **Customer Type**: **Transient** customers account for the majority of bookings.
-   **Market Segment**: **Online TA** (Travel Agent) is the dominant market segment.
-   **Deposit Type**: **No Deposit** is overwhelmingly the most preferred deposit type.

### 4. Stay Duration and Revenue
-   **Stay Duration**: In City Hotels, most guests stay for **3 days**, while in Resort Hotels, most stay for **1 day**.
-   **Revenue Generation**: **City Hotels** generate more revenue than Resort Hotels.
-   **Waiting Time**: **City Hotels** have a longer average waiting period.
-   **Average Daily Rate (ADR)**:
    -   City Hotels generate more revenue in May, while Resort Hotels peak between July and August.
    -   **GDS (Global Distribution System)** contributes most to ADR.

### 5. Correlation Insights
-   `lead_time` and `total_stay` are positively correlated.
-   `adults`, `children`, and `babies` are correlated with each other, and generally, more people lead to a higher ADR.
-   `is_repeated_guest` and `previous_bookings_not_canceled` show a strong correlation, suggesting repeated guests are less likely to cancel.

## Recommendations for Stakeholders
1.  **Strategic Cancellation Management**: For City Hotels, investigate the root causes of higher cancellations and implement dynamic pricing, flexible cancellation policies, or personalized retention offers.
2.  **Optimize Seasonal Strategies**: Leverage peak booking months (July/August) with targeted promotions. Analyze the reasons for the booking drop in 2017 to recover and sustain growth. Develop attractive packages for off-peak seasons.
3.  **Targeted Marketing**: Focus marketing efforts on key demographics, especially the Portuguese market, and consider integrating cultural preferences into services. Continue to highlight the popular 'BB' meal plan.
4.  **Enhance Booking Channel & Room Allocation**: Strengthen partnerships with high-performing travel agents (e.g., Agent #9). Address the discrepancy between reserved and assigned room types to improve guest satisfaction and reduce potential cancellations.
5.  **Boost Resort Hotel Stays & Revenue**: Implement strategies to encourage longer stays in Resort Hotels, such as value-added packages or activity bundles. Analyze and adjust pricing (ADR) based on seasonal demand and distribution channel performance (noting GDS's high ADR).
6.  **Cultivate Guest Loyalty**: Introduce and actively promote a comprehensive loyalty program offering exclusive benefits (discounts, upgrades, personalized services) to increase the low rate of repeated guests.
