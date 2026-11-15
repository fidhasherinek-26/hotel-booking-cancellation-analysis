# 🏨 Hotel Booking & Cancellation Analysis

## 📌 Project Overview

This project analyzes hotel booking data to identify factors associated with booking cancellations and generate actionable business insights for improving cancellation management.

The project combines **data cleaning, exploratory data analysis, statistical hypothesis testing, effect-size analysis, and data visualization** using Python.

### 🎯 Business Question

> **What factors are associated with hotel booking cancellations, and what actionable insights can hotels use to improve booking management and reduce cancellation risk?**

---

## 📊 Dashboard

![Hotel Booking Cancellation Dashboard](hotel_booking_dashboard.png)

---

## 🛠️ Technologies Used

- 🐍 Python
- 🐼 Pandas
- 🔢 NumPy
- 📊 Matplotlib
- 📈 Seaborn
- 📉 Plotly
- 🔬 SciPy
- ☁️ Google Colab

---



## 📂 Dataset

This project uses the **Hotel Booking Demand** dataset, containing booking information for City Hotel and Resort Hotel.

**Dataset Source:** [Kaggle — Hotel Booking Demand](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand?utm_source=chatgpt.com)

**Original Research Paper:** *Hotel Booking Demand Datasets* by Nuno Antonio, Ana de Almeida, and Luis Nunes, published in *Data in Brief* (2019).


> **Note:** The dataset is used for educational and portfolio analysis purposes. The analysis in this repository is my own work.
Important variables include:

- Hotel type
- Cancellation status
- Lead time
- Length of stay
- Customer type
- Market segment
- Distribution channel
- Deposit type
- ADR (Average Daily Rate)
- Repeated guest status
- Previous cancellations
- Previous successful bookings
- Booking changes
- Special requests
- Room types
- Meal type

---

## 🔍 Project Workflow

### 1. Data Understanding

- Loaded and inspected the dataset
- Examined dimensions and data types
- Analyzed descriptive statistics
- Identified categorical and numerical variables

### 2. Data Cleaning

- Removed duplicate records
- Investigated missing values
- Handled missing country information
- Created additional analytical features
- Checked unusual and rare categories

### 3. Exploratory Data Analysis

Cancellation behavior was analyzed across:

- Hotel type
- Lead time
- ADR
- Customer type
- Market segment
- Deposit type
- Distribution channel
- Repeated guest status
- Previous cancellation history
- Previous successful bookings
- Booking changes
- Parking requirements
- Waiting-list duration
- Stay duration
- Number of adults, children, and babies
- Meal type
- Room-type changes

### 4. Bivariate Analysis

Relationships between multiple booking characteristics and cancellation status were investigated, including:

- Hotel type × Lead time
- Hotel type × Market segment
- Hotel type × ADR
- Market segment × Deposit type
- Hotel type × Stay duration
- Hotel type × Customer type
- Previous successful bookings × Cancellation

### 5. Statistical Hypothesis Testing

The project used statistical tests to determine whether selected booking characteristics were significantly associated with cancellation status.

Tests included:

- **Chi-Square Test of Independence**
- **Mann-Whitney U Test**
- **Cramér's V**
- **Rank-Biserial Correlation**

---

## 📈 Key Findings

### 1. ⏳ Lead Time

Cancellation rates increased substantially as lead time increased.

| Lead Time | Cancellation Rate |
|---|---:|
| 0–30 days | 18.6% |
| 31–60 days | 31.6% |
| 61–120 days | 33.5% |
| 121–180 days | 35.1% |
| 181–365 days | 39.7% |
| 365+ days | **40.9%** |

Lead time showed the **largest effect size among the tested variables**, with a rank-biserial correlation of **0.293**.

---

### 2. 🏨 Hotel Type

| Hotel Type | Cancellation Rate |
|---|---:|
| City Hotel | **30.0%** |
| Resort Hotel | 23.5% |

City Hotel bookings had a higher cancellation rate than Resort Hotel bookings.

---

### 3. 🌐 Market Segment

Online Travel Agent bookings showed a relatively high cancellation rate:

**Online TA — 35.3%**

Corporate bookings had a considerably lower cancellation rate:

**Corporate — 12.1%**

---

### 4. 👥 Returning Customers

Repeated guests showed substantially lower cancellation rates.

| Guest Type | Cancellation Rate |
|---|---:|
| Non-repeated Guest | 28.3% |
| Repeated Guest | **7.6%** |

This suggests that returning customers represent a relatively reliable booking segment.

---

### 5. 💳 Deposit Type

Non-refundable bookings showed an exceptionally high cancellation rate:

**94.7%**

This should be interpreted as an **association rather than evidence of causation**.

---

### 6. 👤 Customer Type

Cancellation rates varied considerably across customer types.

| Customer Type | Cancellation Rate |
|---|---:|
| Transient | **30.1%** |
| Contract | 16.3% |
| Transient-Party | 15.2% |
| Group | 9.9% |

Transient bookings represented the highest cancellation-risk segment among the customer types analyzed.

---

## 🔬 Statistical Evidence

All six tested variables showed statistically significant relationships with cancellation status.

| Variable | Statistical Test | Effect Size |
|---|---|---:|
| Customer Type | Chi-Square | 0.127 |
| Lead Time | Mann-Whitney U | **0.293** |
| ADR | Mann-Whitney U | 0.185 |
| Total Stay Duration | Mann-Whitney U | 0.133 |
| Repeated Guest | Chi-Square | 0.090 |
| Deposit Type | Chi-Square | 0.165 |

The results show that **statistical significance does not necessarily mean a strong practical relationship**. Among the variables tested, lead time showed the largest effect size.

---

## 💡 Business Recommendations

Based on the analysis, hotels could:

### 1. Monitor long-lead-time bookings
Prioritize bookings made far in advance for proactive confirmation and cancellation-risk monitoring.

### 2. Monitor Online TA bookings
Online Travel Agent bookings showed relatively high cancellation rates and may benefit from closer monitoring.

### 3. Develop hotel-specific strategies
City Hotel showed a higher cancellation rate than Resort Hotel, suggesting that cancellation-management strategies could be tailored by hotel type.

### 4. Strengthen customer retention
Returning guests showed considerably lower cancellation rates. Loyalty programs and personalized offers could help strengthen this customer segment.

### 5. Monitor multiple risk characteristics
Hotels should consider lead time, customer history, market segment, stay duration, ADR, and other booking characteristics together rather than relying on a single variable.

---

## 📁 Project Files

```text
hotel-booking-cancellation-analysis/
│
├── README.md
├── hotel_booking_cancellation_analysis.ipynb
└── hotel_booking_dashboard.png
```

### Notebook

The Jupyter/Google Colab notebook contains the complete analysis, including data cleaning, EDA, statistical testing, visualizations, business insights, and recommendations.

### Dashboard

The dashboard provides a visual summary of the major cancellation patterns and business findings.

---

## 🎯 Conclusion

The analysis demonstrates that hotel cancellation behavior is associated with several booking characteristics, particularly **lead time, hotel type, market segment, customer history, ADR, customer type, and deposit type**.

Longer lead times were associated with higher cancellation rates, while returning customers showed substantially lower cancellation rates.

Statistical testing confirmed significant relationships between the selected variables and cancellation status. However, the effect sizes were generally modest, emphasizing the importance of considering multiple factors together.

Overall, this project demonstrates how **Python-based data analysis, statistical reasoning, and visualization can transform raw hotel booking data into actionable business insights**.

---

## 👩‍💻 Author

**Fidhasherin E.K.**


**Interests:** Data Analytics • Machine Learning • Statistical Analysis • Python
