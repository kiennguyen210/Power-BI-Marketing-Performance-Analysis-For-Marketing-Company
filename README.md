# Marketing Performance Analysis For Marketing Campaign (Retail Company) | Power BI

<img width="2560" height="1707" alt="Image" src="https://github.com/user-attachments/assets/e59fd733-9227-4646-82ac-cbd16fd6fe24" />

*How to optimally allocate marketing budget across channels, campaigns and regions to maximize Return on Ad Spend (ROAS) by using Power BI?*

---

**Author:** Nguyễn Duy Kiên

**Date:** October 2025

**Tools Used:** Power BI

---

## 📑 Table of Contents  
1. [📌 Background & Overview](#1--background--overview)  
2. [📂 Dataset Description & Data Structure](#2--dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#3--design-thinking-process)  
4. [📊 Key Insights & Visualizations](#4--key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#5--final-conclusion--recommendations)

---

## 1. 📌 Background & Overview

### 1.1. Objective:

This project is a deep-dive marketing performance dashboard built on Power BI. Its primary goal is to shift the focus from simple spending analysis to actual Marketing ROI (Return on Investment), ROAS (Return on Ad Spend) and profitability.

- Measure Marketing ROAS across every layer: campaign, channel, and location.

- Support Data-Driven Budget Allocation decisions by identifying the most profitable marketing sources.

- Define Optimal Strategy for media channels (which channel to scale) and geographic markets (which region to focus on).

### 1.2. What is this project about?

✔️ This project tackles the critical business question: "Where are we making money, and where are we losing it?"

✔️ It helps us understand the relationship between spending (Cost) and profitability (ROAS/Profit Margin).

✔️ The dashboard breaks down overall marketing success into two clear viewpoints: Campaign overview & Market detail

✔️ The analysis provides a comprehensive view of the marketing funnel, from Impressions to Conversions, allowing for specific optimizations at every stage.

✔️ By focusing on metrics like ROAS and Profit Margin, the project provides actionable data to stop wasting budget on underperforming areas and double down on proven successes.

### 1.3. Who is this project for?

This dashboard is designed to provide clear, immediate value to key decision-makers who manage marketing resources and strategy:

👤 Marketing Managers: To monitor performance, report ROI to stakeholders, and adjust strategy dynamically.

👤 Media Buyers & Specialists: To quickly identify underperforming campaigns, channels, or ads that require immediate optimization.

👤 Finance & Budgeting Teams: To understand the true profitability and cost-effectiveness of marketing investments.

👤 Business Analysts: To conduct in-depth investigations into market performance (Location) and user experience (Device).

## 2. 📂 Dataset Description & Data Structure

### 2.1. Data Source  
- Source: Company database. 
- Size: 9901 rows & 18 columns 
- Format: .xlsx

### 2.2. Data Structure & Relationships 

#### 1️⃣ Tables Used:  
This dataset has only 1 single fact table with all information including dim, so I decided to split it into 1 single fact table along with 6 dim tables corresponding to 6 dimensions that I want to analyze throughout this dataset.

#### 2️⃣ Table Schema & Data Snapshot  

| Campaign                    | Marketing campaign                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------|
| Date                        | Date for daily ad performance metrics                                                             |
| City/Location               | Cities that were targeted by campaign                                                             |
| Latitude                    | Latitude for the cities                                                                           |
| Longitude                   | Longitude for the cities                                                                          |
| Channel                     | Channel where ads where displayed (Facebook, Instagram, Pinterest)                                |
| Device                      | Device from ads where viewed                                                                      |
| Ad                          | Ads that where used within a campaign                                                             |
| Impressions                 | Daily impressions (times ad was shown to a viewer) for each ad                                    |
| CTR, %                      | Daily average click-through rate for each ad                                                      |
| Clicks                      | Daily clicks for each ad                                                                          |
| Daily Average CPC           | Daily average cost-per-click for each ad                                                          |
| Spend, GBP                  | Total daily amount of advertising spending for each ad, in GBP                                    |
| Conversions                 | Total daily purchases attributed to a specific ad                                                 |
| Total conversion value, GBP | Total amount in GBP received from purchases attributed to a specific ad                           |
| Likes                       | Total daily likes (or other reactions) per ad                                                     |
| Shares                      | Total daily shares per ad. For the simplicities sake, each Pin on Pinterest is counted as a share |
| Comments                    | Total daily comments per ad                                                                       |

#### 3️⃣ Data Relationships

<img width="2041" height="1106" alt="image" src="https://github.com/user-attachments/assets/5c047fd9-b938-4b6a-96bb-2695dbd712b7" />

## 3. 🧠 Design Thinking Process

### 3.1. Empathize  

<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/23e35325-5699-41d2-ad6b-0f546389cfc2" />

### 3.2. Define point of view  

<img width="1920" height="1080" alt="2" src="https://github.com/user-attachments/assets/324b8d6a-1306-4b58-9b2c-28362449cdb3" />

### 3.3. Ideate 

<img width="1920" height="1080" alt="3" src="https://github.com/user-attachments/assets/f20afadb-95f5-47c3-a96b-898a95e48811" />

## 4. 📊 Key Insights & Visualizations

### 4.1. Campaign Overview

<img width="8831" height="5025" alt="Project_Final_Page_1" src="https://github.com/user-attachments/assets/bdc48f7c-cc81-4417-9333-64208740c5b7" />

| Category                                   | Insights                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| 1. High-level Performance (Scorecards)     | - "North Star" Metrics: The campaign achieved an overall ROAS of 10.61 and an ROI of 9.61, demonstrating exceptional capital efficiency ($1 of ad spend generates $10.61 in revenue). - Financial Scale: Total Revenue reached $1.73M against a Total Spend of $163.25K, resulting in a Net Profit of $1.57M. - Engagement & Quality: The Engagement Rate stands at 5.46%, and the final Conversion Rate is 22.17%.                                                                                                 |   |
| 2. Channel Performance (Channel Breakdown) | - Pinterest – "The Profit Engine": Despite receiving only 17.3% ($28.24K) of the budget, Pinterest delivered a record-breaking 22.47 ROAS. It is the highest-performing channel but currently the least invested in. - Facebook – Lowest Efficiency: Facebook received the largest budget allocation (43.87% ~ $71.61K) but yielded the lowest ROAS at 5.76. - Instagram – The Balanced Performer: With 38.83% of the budget, Instagram maintained a stable 10.80 ROAS, contributing consistently to total revenue. |   |
| 3. Seasonal Insights (Campaign Parameters) | - Summer – Peak Efficiency: The Summer campaign achieved the highest efficiency with a 14.09 ROAS, despite accounting for only 21.06% ($34.38K) of total spend. - Fall – High Volume, Low ROAS: This period saw the heaviest investment (48.58% ~ $79.31K) and generated the highest revenue ($749K), but ROAS dropped to its lowest at 9.44. This suggests performance saturation as spending scales rapidly. - Spring – Stable Contribution: Contributed moderate revenue with a steady ROAS of 10.06.            |   |
| 4. Time-Series Analysis (Monthly Trends)   | - Year-End Surge: Revenue and Profit trended sharply upward from September to November, peaking in November with $259K in revenue. - Spend-Revenue Correlation: Increased ad spend starting in September ($27K) triggered a significant revenue leap compared to the low-activity period of June–August. - Social Engagement Trends: Impressions, Likes, Comments, and Shares all showed a synchronized upward trend starting in September, indicating peak brand virality.                                         |   |
| 5. Conversion Funnel Insights              | - Funnel Drop-off: From 14.65M total impressions, only 1.24% of users clicked the ads (0.18M clicks). - Closing Efficiency: Although the Click-Through Rate (CTR) is low, the purchase rate for users who visit the site is very high (22.17%). This proves the ads are reaching the right high-intent audience, but the creative content may need optimization to improve the initial CTR.                                                                                                                         |   |

### 4.2. Analytics Detail

<img width="8831" height="5025" alt="Project_Final_Page_2" src="https://github.com/user-attachments/assets/f072d547-9f5e-4aa2-a569-8aa07728855f" />

## 5. 🔎 Final Conclusion & Recommendations



🎯 **Key Takeaways:**



