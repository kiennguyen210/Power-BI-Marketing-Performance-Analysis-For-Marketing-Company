# Marketing Performance Analysis For Marketing Company (Retail Company) | Power BI

<img width="2560" height="1707" alt="Image" src="https://github.com/user-attachments/assets/e59fd733-9227-4646-82ac-cbd16fd6fe24" />

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

This project is a deep-dive marketing performance dashboard built on Power BI. Its primary goal is to shift the focus from simple spending analysis to actual Marketing ROI (Return on Investment) and profitability.

- Measure Marketing ROI across every layer: campaign, channel, and location.

- Support Data-Driven Budget Allocation decisions by identifying the most profitable marketing sources.

- Define Optimal Strategy for media channels (which channel to scale) and geographic markets (which region to focus on).

### 1.2. What is this project about?

✔️ This project tackles the critical business question: "Where are we making money, and where are we losing it?"

✔️ It helps us understand the relationship between spending (Cost) and profitability (ROAS/Profit Margin).

✔️ The dashboard breaks down overall marketing success into six clear viewpoints: Total Performance, Campaigns, Channels, Locations, Devices, and Ad Creatives.

✔️ The analysis provides a comprehensive view of the marketing funnel, from Impressions to Conversions, allowing for specific optimizations at every stage.

✔️ By focusing on metrics like ROAS and Profit Margin, the project provides actionable data to stop wasting budget on underperforming areas and double down on proven successes.

### 1.3. Who is this project for?

This dashboard is designed to provide clear, immediate value to key decision-makers who manage marketing resources and strategy:

👤 Marketing Managers & Directors: To monitor performance, report ROI to stakeholders, and adjust strategy dynamically.

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

#### 1️⃣ 5W1H

<img width="1920" height="1080" alt="pic1" src="https://github.com/user-attachments/assets/0fe80e6a-ab0b-4354-ac27-ef996f3e2684" />

#### 2️⃣ Empathy Maps

<img width="1920" height="1080" alt="pic 2" src="https://github.com/user-attachments/assets/a6263ad4-0d48-4880-81be-67bcd41aafef" />

### 3.2. Define point of view  

#### 1️⃣ Northstar Metric

<img width="1920" height="1080" alt="pic 3" src="https://github.com/user-attachments/assets/364747d6-1e8d-4053-95e6-f095f3eb2afd" />

#### 2️⃣ Define Point Of View

<img width="1920" height="1080" alt="pic 4" src="https://github.com/user-attachments/assets/3d1c4182-97eb-4156-b1a1-fa12e7ea5fbb" />

#### 3️⃣ Growth Fomula

<img width="1920" height="1080" alt="pic 5" src="https://github.com/user-attachments/assets/fe8ef100-c8a8-4e13-8e83-3d95439a4fb2" />

### 3.3. Ideate 

#### 1️⃣ Brainstorming

<img width="1920" height="1080" alt="pic 6" src="https://github.com/user-attachments/assets/f3e2fc65-0b1a-4a0b-8ade-ca8e6c56ed07" />

#### 2️⃣ Structure Idea

<img width="1920" height="1080" alt="pic 7" src="https://github.com/user-attachments/assets/b24f2592-3126-4f22-9908-5c3aad6e1365" />

## 4. 📊 Key Insights & Visualizations

### 4.1. Overview

![Project 4 - Lần 3 3 pdf_Page_1](https://github.com/user-attachments/assets/3a02274a-0893-40cf-95df-a2fd404e6cef)

| Insight                                                                                                                                                                      | Supporting Data                                                                                                                                                                     | Optimization Action                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sharp Seasonal Profitability: ROAS and Profitability show a significant spike in the Summer season, peaking in July and August, followed by a steep decline towards Fall/Q4. | The ROAS Trend chart shows a peak of 14.68 in July. The Revenue, Spend vs Profit chart confirms the highest profit margins during these months.                                     | Concentrate the largest budget allocation during the Summer season and investigate the reasons for the drop in Fall. Set lower CPA/ROAS targets for Q4 due to naturally lower performance. |
| Spend Distribution vs. ROAS Discrepancy: Instagram accounts for the largest share of Total Spend (39.83%), but Facebook and Pinterest deliver a better overall ROAS.         | The Spend Distribution chart shows Instagram highest. The ROAS Decomposition shows Instagram (25.81) is lower than Facebook (39.23) and Pinterest (23.53) in the overall breakdown. | Re-evaluate high spending on Instagram. Reallocate a portion of the budget from Instagram to Facebook (which has a higher ROAS) to increase total profit.                                  |

### 4.2. Campaign

![Project 4 - Lần 3 3 pdf_Page_2](https://github.com/user-attachments/assets/b7110e8d-82fa-4bf3-9736-0112744b3120)

| Insight                                                                                                                                                                  | Supporting Data                                                                                                                                          | Optimization Action                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| The Summer Campaign is the Core Growth Driver: This campaign yields the highest ROAS and the best CPA performance but has not received the corresponding highest budget. | All Campaign KPI Detail: Summer has ROAS 14.09 and CPA 4.09, significantly better than Spring (ROAS 10.06, CPA 3.93) and Fall (ROAS 9.44, CPA 5.33).     | Increase the budget for the Summer Campaign in future cycles. Analyze the creative structure and messaging of the Summer campaign for replication in other periods. |
| The Fall Campaign is High-Cost and Low-Performing: Despite receiving the largest budget allocation, Fall has the highest CPA and lowest ROAS.                            | All Campaign KPI Detail: Fall has Spend 79,313.93 and CPA 5.33. The Spend, Revenue, CPA Scatter Plot positions Fall in the High Spend/Low ROAS quadrant. | Immediately pause or urgently optimize the Fall Campaign. Perform a deep-dive analysis into the channels and creatives within Fall to eliminate budget waste.       |

### 4.3. Channel

![Project 4 - Lần 3 3 pdf_Page_3](https://github.com/user-attachments/assets/a54a1357-e698-4f09-8134-bae9cbda27a6)

| Insight                                                                                                                                                      | Supporting Data                                                                                                                                                         | Optimization Action                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pinterest is the Most Profitable Channel: This channel delivers the highest ROAS and the lowest CPA among the three, demonstrating superior cost-efficiency. | All Channel KPI Detail: Pinterest leads with ROAS 22.47 and CPA 2.45. The ROAS, CPA, Conversions Volume bubble chart shows Pinterest in the high-ROAS, low-CPA cluster. | Prioritize and allocate more budget to Pinterest. The goal is to maximize profit before this channel reaches its point of budget saturation.                                    |
| Instagram is the Least Profitable in Margin: Instagram has high spend but the worst profit margin percentage per conversion among the channels.              | All Channel KPI Detail: Instagram has a Profit % of 90.74% (the lowest) and a CPA of 4.07 (second highest).                                                             | Focus on optimizing or reducing the Instagram budget. Analyze the campaigns and ad creatives on Instagram (Page 6) to pinpoint the specific elements causing low profitability. |

### 4.4. Location

![Project 4 - Lần 3 3 pdf_Page_4](https://github.com/user-attachments/assets/fd0248ca-b68e-4fac-9af0-06f458780456)

| Insight                                                                                                                                                                             | Supporting Data                                                                                                                                                                                      | Optimization Action                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manchester Shows Highest Market Purchasing Power and Profit: This region provides the highest ROAS across all channels, indicating a high-intent market with strong responsiveness. | All Location & Channel KPI Detail: Manchester leads with an overall ROAS of 27.93 and CVR of 19.52%. The ROAS, Revenue, Spend Scatter Plot places Manchester in the High ROAS/High Revenue quadrant. | Prioritize budget and strategic growth efforts in Manchester. Increase impression share and media density in this high-performing market.                                                         |
| London is the Least Cost-Effective Market: Despite relatively high spend, London has the lowest ROAS, particularly on the Facebook channel.                                         | All Location & Channel KPI Detail: London has an overall ROAS of 17.93%. London's Facebook ROAS is only 4.86, significantly lower than Birmingham (5.33) and Manchester (7.08).                      | Adjust channel strategy by region: Immediately reduce CPA targets/budget on Facebook in London. Analyze why Instagram and Pinterest perform significantly better in London (ROAS 25.4 and 34.83). |

### 4.5. Device

![Project 4 - Lần 3 3 pdf_Page_5](https://github.com/user-attachments/assets/902d7411-f57b-4509-9382-ec5c982e0e31)

| Insight                                                                                                                                                                                                        | Supporting Data                                                                                                                                                                                                                                | Optimization Action                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobile CVR is Worse than Desktop: Although Mobile ROAS shows higher peaks in the first half of the year, the average Conversion Rate (CVR) on Mobile is lower than Desktop, suggesting user experience issues. | CVR Trend by Device: Desktop CVR is consistently higher than Mobile CVR in recent months (Desktop 17.75% vs. Mobile 14.15% in Oct). The Conversion Funnel by Mobile shows a low Clicks -> Conversion rate (0.21%) compared to Desktop (0.37%). | Focus on optimizing the Mobile Shopping Experience: Analyze Mobile Page Load Speed and the checkout process to improve the CVR funnel.                                  |
| Mobile ROAS Deteriorates with High Spend: The mobile channel shows good ROAS in smaller, seasonal campaigns, but the ROAS declines sharply when spend increases (e.g., in the 'Full' campaign).                | Clicks, CPC, CTR by Device: Mobile (Summer) has ROAS 14.25 vs. Desktop (13.75). However, when transitioning to the largest campaigns (Full), Mobile's ROAS is lower.                                                                           | Be cautious when scaling the Mobile budget: Implement a budget cap on Mobile and only allocate increased funds to highly optimized campaigns to maintain profitability. |

### 4.6. Ad Creative

![Project 4 - Lần 3 3 pdf_Page_6](https://github.com/user-attachments/assets/41b61c4e-e157-4caf-a1f9-f4bdd0ed8cae)

| Insight                                                                                                                                                                         | Supporting Data                                                                                                                                                                                                      | Optimization Action                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| The "Discount" Ad Creative Drives High Conversion and Low Cost: The advertising strategy focusing on offers (Discount) has the highest CVR and the lowest Cost per Conversions. | Conversions, CPA, CVR by Ad: Discount has the highest CVR (37%) and lowest Cost per Conversions (4.06) compared to Collection (5.46%). The CVR, CTR, CPA by Ad Scatter Plot shows Discount in the high-CVR position. | Scale up "Discount" focused ads. Leverage offer messaging to attract high-intent customers. Ensure the profit margin is maintained after the discount is applied.                                                                                            |
| The "Collection" Ad Creative Has High Engagement but Low CVR: While attracting high engagement, the Collection ad creative has a low conversion rate and a high CPA.            | Engagement Rate: Collection has an Engagement Rate of 5.46%. CPA: Collection has a high CPA (6.24) compared to Discount (4.06).                                                                                      | Re-evaluate the Landing Page experience for the Collection ad. If the ad is compelling (high engagement), the drop-off is likely occurring on the landing page or due to product relevance. Optimize the destination page to convert engagement into orders. |

## 5. 🔎 Final Conclusion & Recommendations

| Observation                                                                                                                                                                                                             | Implication                                                                                                | Strategic Recommendation                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| High Spend in Low-ROAS Areas: Instagram and the "Fall" Campaign consume the largest budgets but deliver the lowest ROAS (Instagram ROAS: 25.81; Fall ROAS: 9.44).                                                       | Budget is being wasted in high-volume, low-efficiency placements, restricting funds from profitable areas. | Budget Reallocation (Shift Focus): Immediately shift 20-30% of the Instagram and Fall Campaign budgets to the proven profit drivers: Pinterest (ROAS 22.47) and the Summer Campaign (ROAS 14.09).                                                              |
| Geographic Disparity in Market Purchasing Power: Manchester is the clear high-value market (ROAS 27.93), while London, particularly on Facebook (ROAS 4.86), is highly inefficient.                                     | Profitability is market-dependent and channel strategies must be localized, not universal.                 | Geo-Targeting Refinement (Scale & Reduce): Scale investment in Manchester to maximize returns. For London, perform a surgical cut on Facebook spend and reallocate those funds to better-performing local channels (Instagram/Pinterest).                      |
| Funnel Leakage on Mobile and General Creatives: Mobile CVR is consistently lower than Desktop (Mobile CVR 14.15% vs Desktop 17.75%), and the "Collection" ad creative generates high engagement but low CVR (CPA 6.24). | User experience and landing page relevancy are bottlenecking conversions and increasing CPA.               | Conversion Rate Optimization (Fix Leaks): Prioritize Mobile Site optimization (speed, checkout). Review the landing pages linked to "Collection" ads to ensure the page content matches the user intent generated by the ad, converting engagement into sales. |

🎯 **Key Takeaways:**

1. Profitability Driver: The fastest path to increased ROI is by aggressively scaling Pinterest and the Summer Campaign while maintaining strict CPA limits.

2. Market Focus: Treat Manchester as the priority growth market and implement a highly specific, localized channel strategy for London.

3. Experience Fix: Immediate action is required to repair the Mobile CVR gap and optimize Landing Page performance for general awareness creatives.

