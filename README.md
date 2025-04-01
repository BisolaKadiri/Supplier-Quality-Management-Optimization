# Supplier-Quality-Management-Optimization

## Overview
Effective management of raw material quality is crucial for manufacturers to maintain operational efficiency, reduce downtime, and minimize costs. However, many organizations face significant challenges due to supplier inconsistencies, resulting in material defects that disrupt production and incur additional costs. Managing supplier quality across multiple plants further complicates this, especially when no centralized system exists to track and evaluate supplier performance. Business Intelligence (BI) tools, such as Power BI, can address these challenges by consolidating supplier data and providing actionable insights for decision-making, ultimately improving supplier relationships and reducing production risks.

## Problem Statement
Enterprise Manufacturers Ltd. faced difficulties in validating and tracking supplier performance across various plants, leading to frequent downtime and inconsistent production outputs. The absence of a centralized system hindered visibility into supplier quality, preventing the company from addressing performance gaps. To improve the situation, the management team posed the following key questions:

1. Which vendors/plants are contributing to the highest defect quantities?
2. Which vendors/plants are causing the most downtime?
3. Are there any combinations of materials and vendors that consistently result in defects?
4. How does the performance of the same vendor/material vary across different plants?
5. Are there overlooked insights or patterns that could help mitigate supplier-related issues?

To answer these questions, a data-driven approach was essential.

## Analysis Approach
The primary goal was to quantify the financial impact of defective materials on production efficiency and to identify the main contributors—vendors, plants, and materials. Rather than presenting abstract metrics like the total number of defective units or downtime minutes, the focus was on showcasing the tangible financial impact of these problems, helping stakeholders understand how much money was being lost due to poor supplier performance.

## Key aspects of the approach included:
1. Understanding the Business Needs: The company lacked a procurement system, and their primary objective was to monitor and improve the quality of goods sent by suppliers.
2. Focus on Financial Implications: The analysis aimed to highlight the direct financial loss caused by defective materials, offering a clearer picture of how supplier quality issues affect the bottom line.
3. Actionable Insights: Instead of merely identifying defective materials, the goal was to identify patterns and sources of these defects across vendors, materials, and plants.

## Dataset Overview
The dataset used for the analysis contained the following key attributes:
- Date: When the defect was recorded.
- Vendor: The supplier of the material.
- Plant Location: The geographic site of the plant where the material was used.
- Category: The classification of the material.
- Material Type: The type of material used.
- Defect Type: The classification of the defect.
- Defect: A brief description or code for the defect type.
- Total Defect Quantity: The total number of defective materials recorded.
- Total Downtime Minutes: The total number of downtime minutes caused by the defective material.

## Methodology
To efficiently manage the dataset and improve report generation, a star schema data model was implemented. This involved segmenting the data into fact and dimension tables for better performance and reporting.

## Steps in the Methodology:
1. Segmentation into Dimension Tables: Key attributes such as Vendor, Plant Location, Material Type, and Defect Type were split into separate tables. This streamlined the dataset and facilitated better querying.
2. Building the Fact Table: The fact table contained core metrics, including defect quantity and downtime minutes, and was linked to the dimension tables via unique identifiers.
3. Date Table: A dedicated Date Table was created using DAX, enabling effective time-series analysis and the application of time-related filters.
4. Star Schema Data Model: Relationships were established between dimension tables and the fact table to form a star schema, optimizing reporting and query performance.

## Dashboard Design and Analysis
Once the data was structured and modeled, the next step was to design a user-friendly dashboard that would deliver actionable insights at a glance. The dashboard needed to cater to both high-level executives and operational teams, providing clear insights into key metrics.

## Key Metrics:
- Downtime: The total number of hours lost due to defective materials.
- Defect Quantity: The total number of defective units received from suppliers.
- Downtime Cost: The financial impact of downtime, calculated at $10 per hour of downtime.

## Key Features:
- Overview Page: A snapshot of the critical metrics, including total defects, downtime hours, and the financial impact (Downtime Cost). The page included a monthly trend chart for defect quantities and downtime hours, along with a Worst Performers section for vendor, plant, and material breakdowns.
- Vendor Performance: A Top N Analysis of vendors based on defect quantity or downtime hours, categorized into high, medium, and low-risk groups based on their contribution to downtime. This feature enabled targeted analysis of supplier performance.
- Plant Performance: A map showing the geographic distribution of plants and their performance, along with a detailed breakdown of defects by location. This section also included a tooltip with additional metrics for each plant.
- Material Performance: A breakdown of defect impact by material type, defect type, and category, with a focus on problematic materials like Logistics and Mechanicals defects.
- Downtime Impact: This section highlighted the financial impact of downtime, with specific dates and periods (such as September and December) where downtime costs spiked.

## Key Insights
- Rising Defects and Downtime: The company experienced 2.6 billion defective units and 216,000 hours of downtime, leading to a $2.16 million financial impact.
- Financial Impact: The direct correlation between downtime and financial losses was evident, with certain periods (September and December) causing the most significant disruptions.
- Worst-Performing Vendors: Vendors such as Avamm, Meejo, and Yombu were identified as high-risk due to their substantial contribution to defects and downtime.
- Plant-Specific Issues: Plants like Hingham, Charles City, and Twin Rocks were major contributors to defects and downtime.
- Material Performance: Mechanical and Logistics defects showed rising trends, indicating potential issues with equipment maintenance and supply chain management.

## Recommendations
1. Centralize Data and Automate Reporting: A centralized system should be implemented to track supplier performance across plants, automating data collection and reporting to enhance consistency.
2. Focus on Financial Impact: Manufacturers should prioritize the financial impact of downtime, ensuring decision-makers have a clear view of the cost implications.
3. Implement Continuous Improvement Programs: A continuous improvement program focused on reducing downtime and addressing recurring defects will drive accountability and process improvements.
4. Leverage Advanced Analytics: Predictive models and advanced analytics can be used to identify and address issues early, preventing costly downtime and material waste.

## Conclusion
By leveraging business intelligence tools like Power BI, Enterprise Manufacturers Ltd. was able to transform raw data into actionable insights, identifying key suppliers, plants, and materials contributing to production inefficiencies. The implementation of this BI-driven approach not only highlighted operational inefficiencies but also paved the way for data-driven improvements across the supply chain. Centralizing procurement and performance data will allow the company to make more informed decisions, improve supplier relationships, and reduce production costs.
