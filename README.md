# Marketing-Efficiency-BI-Reporting

##  Project Overview

This repository contains an enterprise Business Intelligence and Reporting suite built in Power BI. Analyzing a 5,000-record dataset of digital marketing interactions, this project bridges the gap between top-of-funnel marketing investments and bottom-of-funnel product outcomes. The primary objective is to provide a transparent, data-driven view of campaign profitability, customer acquisition efficiency, and product conversion rates.

##  Business Value & Objectives

* **Financial Accountability:** Delivered clear visibility into Return on Ad Spend (ROAS) and Customer Acquisition Cost (CAC) to identify which marketing channels drive profitable product adoption versus which burn budget.
* **Product Analytics:** Shifted the focus from vanity metrics (clicks and impressions) to true product outcomes (conversions and revenue generation).
* **Enterprise Reporting:** Built a scalable, intuitive interface for stakeholders ranging from C-suite executives to marketing managers, enabling rapid, confident decision-making.

##  Dashboard Architecture & UI/UX

The application is structured using a clean, grid-based executive layout designed for immediate scannability.

* **Executive KPI Banner:** Dynamic tracking of Total Ad Spend, Total Revenue, Total Conversions, CAC, and ROAS.
* **Macro Diagnostics:** Features a dual-axis clustered column/line chart to safely compare high-volume Revenue against lower-volume Ad Spend without skewing visual scales, instantly highlighting profitable channels.
* **Efficiency Matrix:** A scatter plot evaluating Conversion Rate against CAC, categorizing campaigns into visual quadrants of efficiency.
* **Granular Deep-Dive:** A detailed matrix report providing marketing managers with exact decimal-point breakdowns of CTR, Conversion Rates, and ROAS across every individual campaign.

##  Technical Stack & Skills Demonstrated

**Business Intelligence & Reporting**

* **Tool:** Power BI Desktop
* **Data Transformation:** Power Query (Engineered a robust ETL pipeline utilizing a master staging query to feed downstream tables).
* **Data Modeling:** Optimized Star Schema architecture, separating the raw flat file into distinct Dimension tables (`dim_user`, `dim_campaign`, `dim_channel`) and a central Fact table (`fact_marketing_performance`) to handle multi-touch interaction logic flawlessly.

**Advanced DAX (Data Analysis Expressions)**

* Engineered dynamic financial and product analytics measures to ensure accurate recalculation across all executive slicers.
* Implemented `DIVIDE()` functions for all efficiency ratios (CTR, Conversion Rate, CAC, ROAS) to handle evaluation contexts securely and prevent zero-division errors.

##  Dataset Information

* **Source:** Causal Digital Marketing Campaign Dataset.
* **Scope:** 5,000 distinct marketing interactions spanning multiple channels (Search, Social, Display, Video, Email) and product segments.
* **Note:** The data model accommodates multi-touch attribution scenarios, correctly tracking unique users who interacted with multiple campaigns across different channels prior to conversion.

##  Strategic Recommendations
Based on the diagnostic metrics engineered in this reporting suite, several actionable business intelligence insights were identified:

*   **Reallocate Marketing Spend for Profitability:** By analyzing the Return on Ad Spend (ROAS) across all channels, it is clear that specific channels (e.g., Search and Social) yield a disproportionately higher financial return. Budget should be shifted away from low-efficiency channels (like Display) to maximize overall revenue.
*   **Investigate High-Friction Channels:** Campaigns that display a high Click-Through Rate (CTR) but a significantly low Conversion Rate indicate a disconnect between marketing copy and the product landing page. Product and UI/UX teams should investigate these specific user journeys to reduce friction and improve the sign-up flow.
*   **Targeted Device Optimization:** The discrepancy in Customer Acquisition Cost (CAC) between Mobile and Desktop platforms suggests that ad formats or product landing pages are not universally optimized. Marketing efforts should be tailored to the platform demonstrating the highest user retention and lowest acquisition cost for each distinct product segment.

##  How to Use

1. Download the `.pbix` file from this repository.
2. Open with **Power BI Desktop**.
3. Use the top navigation slicers to filter the dashboard by Channel, Campaign ID, or Product Segment to explore the dynamic reporting capabilities.
