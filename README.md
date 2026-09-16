# Namma Yatri Ride Analytics

## 📊 Project Overview

This project analyses Namma Yatri ride data using **Power BI** to understand ride demand, revenue patterns, customer and driver cancellations, conversion rates, payment behaviour, and zone-level performance.

The objective is to identify operational inefficiencies and generate data-driven recommendations for improving ride conversion, driver allocation, customer experience, and revenue generation.

---

## 🎯 Business Objective

The analysis focuses on:

- Understanding ride demand across different time periods
- Identifying high-demand and high-revenue zones
- Analysing customer and driver cancellation behaviour
- Measuring search-to-ride conversion
- Understanding the relationship between demand and revenue
- Identifying opportunities to improve operational efficiency
- Developing marketing and operational recommendations

---

## 📂 Dataset

The dataset contains information across multiple related tables:

- **Trip Details** – ride searches, quotes, cancellations, OTP entry and ride completion
- **Trips** – fare, distance, driver, customer and location details
- **Payment** – payment methods
- **Assembly** – pickup and destination zones
- **Duration** – hourly time intervals

The dataset was imported into Power BI using the Excel connector.

---

## 🛠️ Tools & Technologies

- Power BI
- DAX
- Data Modelling
- Data Cleaning
- Data Analysis
- Data Visualization
- Excel

---

## 🔗 Data Model

The **Trips** table was treated as the central fact table, with supporting dimension tables for location, payment and time-related information.

Key relationships included:

- `Trip_Details[tripid] → Trips[tripid]`
- `Trips[faremethod] → Payment[id]`
- `Trips[loc_from] → Loc From[ID]`
- `Trips[loc_to] → Loc To[ID]`
- `Trips[duration] → Duration[id]`

A star-schema approach was used for analysis.

---

## 📈 Analysis Performed

### 1. Ride Demand Analysis

Ride demand was measured using the **number of searches** as a proxy for customer demand.

Peak demand periods identified in the analysis include:

- 0–1
- 6–8
- 13–15
- 22–23

Demand varies considerably across different time periods and zones.

### 2. Revenue Analysis

Revenue contribution was analysed across hourly time intervals.

The analysis found that revenue generally moves with demand, but the relationship is not perfectly aligned. Revenue is also influenced by factors such as trip distance and pricing.

### 3. Payment Method Analysis

Payment methods analysed include:

- Credit Card
- Debit Card
- UPI
- Cash

The distribution was relatively balanced, with credit card having the highest ride frequency in the analysed dataset.

### 4. Zone-Level Analysis

The analysis identified high-demand and high-revenue pickup zones.

High-demand zones included:

- Ramanagaram
- Yeshwanthpur
- Bangalore South
- Dasarahalli

High-revenue zones included:

- Bangalore South
- Yeshwanthpur
- Hebbal
- Rajarajeswarinagar

### 5. Cancellation Analysis

Customer and driver cancellation rates were calculated using DAX measures.

| KPI | Result |
|---|---:|
| Customer Cancellation | 48.17% |
| Customer Success | 51.83% |
| Driver Cancellation | 47.25% |
| Driver Success | 52.75% |

### 6. Conversion Analysis

The search-to-ride conversion rate was calculated as:

`Completed Rides / Total Searches`

The overall conversion rate observed in the analysis was **45%**.

This indicates a substantial drop-off between ride searches and completed rides.

### 7. Dynamic Top-N Analysis

A **Top N Zones** parameter was created in Power BI to allow interactive analysis of the highest-volume pickup zones.

The parameter allows users to dynamically examine different numbers of top-performing zones.

---

## 📊 Power BI Dashboard

The interactive dashboard brings together:

- Customer cancellation %
- Customer success %
- Driver cancellation %
- Driver success %
- Conversion rate
- Top N zones
- Ride demand by time
- Demand vs. revenue by time
- Revenue contribution by time
- Ride demand across time by zone

The dashboard enables users to explore ride performance across different locations and time periods.

---

## 🔍 Key Findings

### Demand

- Ride demand varies significantly across time periods.
- Peak demand occurs during specific recurring time intervals.
- Demand also differs considerably between pickup zones.

### Revenue

- Higher demand generally corresponds with higher revenue.
- Demand and revenue are not perfectly aligned.
- Trip distance and pricing can influence revenue independently of demand.

### Operations

- Customer cancellation was **48.17%**.
- Driver cancellation was **47.25%**.
- Overall search-to-ride conversion was **45%**.
- The analysis therefore highlights a substantial gap between ride demand and completed rides.

### Zones

- Ramanagaram and Yeshwanthpur were among the highest-volume zones.
- Bangalore South and Yeshwanthpur were among the leading revenue-generating zones.
- Zone performance varies across time periods.

---

## 💡 Business Recommendations

Based on the analysis, the project proposes:

### Improve Conversion

- Provide accurate ETA and fare estimates
- Reduce customer waiting time
- Improve driver availability during high-demand periods
- Retarget users who drop off after searching

### Reduce Cancellations

- Improve driver-rider matching
- Consider appropriate cancellation policies
- Provide incentives for driver ride completion

### Optimize Driver Allocation

- Increase driver availability during peak demand periods
- Use zone-time based allocation strategies
- Prioritize high-demand zones

### Improve Pricing Strategy

- Analyse demand and revenue together
- Consider localized pricing strategies
- Use off-peak promotional offers where appropriate

### Improve Customer Experience

- Strengthen real-time tracking
- Improve visibility of driver information
- Provide responsive customer support

---

## 📁 Repository Contents

```text
Namma-Yatri-Ride-Analytics/
│
├── Nammayatri_GB.pbix
├── Namma_Yatri_Dashboard.pdf
├── Namma_Yatri_Analysis_Report.pdf
├── Namma_Yatri_Management_Presentation.pptx
├── Namma_Yatri_Technical_Presentation.pptx
└── README.md
```

## 📌 Project Outcome

- This project demonstrates the use of Power BI, DAX, data modelling and business analysis to convert ride-level data into operational and strategic insights.

- The analysis connects customer demand, ride conversion, cancellations, revenue and zone performance to identify areas for operational improvement.

## 👩‍💻 Author

Gayatri Behera

Data Analyst | Python | SQL | Power BI | Machine Learning | Engineering Analytics
