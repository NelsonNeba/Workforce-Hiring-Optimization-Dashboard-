# 🚀 Workforce & Hiring Optimization Dashboard | Power BI

This Power BI dashboard project offers a comprehensive analytical solution for **WorkSmart Retail Inc.**, a multi-state retail company. It provides HR, operations, and leadership teams with actionable insights to optimize workforce deployment, refine recruitment strategies, and enhance overall operational efficiency.

By transforming raw HR and store data into dynamic visualizations, this dashboard empowers data-driven decision-making across various facets of talent management and resource allocation.

---

## 📖 Table of Contents

* [🏢 Business Context](#-business-context)
* [🎯 Project Goals](#-project-goals)
* [✨ Dashboard Highlights](#-dashboard-highlights)
* [📊 Data Sources & Model](#-data-sources--model)
* [🔍 Key Insights & Recommendations](#-key-insights--recommendations)
* [🛠️ Technical Stack & Key Learnings](#%EF%B8%8F-technical-stack--key-learnings)
* [🚀 How to Use the Dashboard](#-how-to-use-the-dashboard)
* [🤝 Contribution & Support](#-contribution--support)
* [📜 License](#-license)

---

## 🏢 Business Context

**Company:** WorkSmart Retail Inc.
**Industry:** Retail (Multi-Store Operations)
**Key Departments Impacted:** Human Resources (HR), Operations, Finance, Sales, Supply Chain, Technology

WorkSmart Retail Inc. aims to enhance its competitive edge by optimizing its workforce and hiring processes. Key challenges included understanding employee distribution, assessing hiring efficiency, managing costs, and aligning staffing with regional needs. This project directly addresses these challenges by providing a centralized, interactive data platform.

---

## 🎯 Project Goals

The primary objective was to develop a **comprehensive and interactive Power BI dashboard** to deliver critical insights into:

* **Hiring Efficiency:** Analyzing costs, trends, time-to-join, and the effectiveness of various hiring modes.
* **Workforce Allocation:** Understanding employee distribution by role, age demographics, and geographical spread across stores.
* **Store Staffing Optimization:** Identifying overstaffed or understaffed stores based on size and regional performance.
* **Compensation Analysis:** Investigating average CTC (Cost to Company) by job title and hiring mode.
* **Relocation Management:** Tracking relocation costs and identifying patterns among relocated hires.

---

## ✨ Dashboard Highlights

The dashboard is designed for intuitive navigation and deep-dive analysis, structured across multiple interactive pages:

> 📷 **Dashboard Screenshot:**
> *(Note: Replace this placeholder with an actual, high-quality screenshot of your Power BI dashboard.)*
> ![Dashboard Screenshot](images/powerbi-dashboard.png)

### Navigable Pages:
* **Overview & KPIs:** A high-level summary of key performance indicators related to hiring and employee demographics.
* **Hiring Analysis:** Detailed breakdown of hiring trends, costs, and mode effectiveness.
* **Employee Demographics:** Visualizations on employee age distribution, job titles, and geographic spread.
* **Store Staffing & Regions:** Insights into store-level employee distribution and regional staffing patterns.
* **Relocation & Cost Deep Dive:** Focused analysis on relocation expenses and their correlation with other hiring metrics.

---

## 📊 Data Sources & Model

The dashboard integrates data from three primary sources, meticulously cleaned and transformed to ensure data integrity and analytical readiness.

| Dataset      | Key Fields Included                                       | Description                                                                  |
| :----------- | :-------------------------------------------------------- | :--------------------------------------------------------------------------- |
| **Employee** | `Employee ID`, `Employee Name`, `Job Title`, `Age`, `Home City`, `Home State`  | Detailed demographic and professional information for each employee.         |
| **Store** | `store_id`, `employees`, `store_size`, `city`, `state`, `region`  | Information on retail store locations, sizes, and current employee counts.   |
| **Hiring** | `hiring_id`, `hiring_date`, `joining_date`, `hiring_mode`, `ctc`, `interviews`, `relocation_cost`, `hiring_cost` | Comprehensive records of the recruitment process, including costs and timelines. |

A robust data model was established in Power BI, connecting these tables to enable cross-dataset analysis and dynamic filtering.

![Model Screenshot](images/powerbi-dashboard.png)
---

## 🔍 Key Insights & Recommendations

The dashboard uncovers critical patterns and provides actionable intelligence:

* **Hiring Cost Efficiency:**
    * The **average hiring cost is approximately $600**.
    * **Newspaper advertising emerges as the most cost-efficient hiring mode**, suggesting a focus for future recruitment drives.
    * Relocation costs show a notable impact on overall hiring expenditure, particularly for certain job titles (e.g., Managers, Finance Executives).

* **Time-to-Join Analysis:**
    * The **average time-to-join ranges between 46 and 54 days**.
    * Hires sourced through **Search Engine channels tend to have longer time-to-join durations**, indicating areas for process optimization or targeted engagement.

* **Employee Demographics & Distribution:**
    * A significant portion of the workforce comprises a **younger demographic**, particularly in Sales and Finance roles, which can inform talent development and retention strategies.
    * Employee concentrations are highest in **California and New York**, aligning with major operational hubs.
    * The average employee age across all stores and roles is visible, allowing for demographic segmentation analysis. 

* **Store Staffing & Regional Imbalances:**
    * Analysis reveals that some **Medium-sized stores are currently overstaffed**, while specific **Large stores are understaffed** in certain regions based on optimal employee-to-store size ratios. This points to opportunities for strategic reallocation.
    * The **West region incurs the highest average hiring costs**, necessitating a review of regional recruitment practices or compensation structures.
    * The dashboard dynamically shows total employees per region and per store size, facilitating quick identification of staffing disparities.
* **Compensation (CTC) Patterns:**
    * **Managerial hires consistently exhibit the highest average CTC (~$70K)**, especially when recruited via Newspaper channels. This insights helps in budgeting and competitive compensation analysis.
    * Observed discrepancies in CTC for similar job roles highlight potential misalignments in compensation strategies, suggesting a need for standardized pay scales or performance-based incentives.

---

## 🛠️ Technical Stack & Key Learnings

This project leveraged a robust set of Microsoft Power BI features and data analysis techniques:

* **Data Extraction & Transformation (ETL):** Utilized **Power Query** to connect to disparate CSV sources, perform data cleaning (handling missing values, standardizing dates, removing duplicates), and transform raw data into a star schema model.
* **Data Modeling:** Established a highly efficient and scalable **star schema data model** with clear relationships between Employee, Store, and Hiring tables, crucial for accurate cross-filter interactions.
* **DAX (Data Analysis Expressions):** Developed complex DAX measures for key metrics such as:
    * `Total Hires`, `Total Hiring Cost`, `Avg Days to Join`, `Average CTC`.
    * `Total Employees in Stores`, `Average Employee Age`, `Total Stores`, `Avg Employees per Store`.
    * `Total Relocation Cost`, `Hires with Relocation`, `Avg Relocation Cost`, `Avg Interviews per Hire`.
    * Calculated `Correlation HiringCost_CTC` to quantify the relationship between these two critical financial metrics.
* **Advanced Visualizations:** Implemented a variety of visual types to tell the data story effectively:
    * **KPI Cards:** For at-a-glance performance monitoring with Year-over-Year (YoY) growth indicators.
    * **Stacked Area Charts:** To visualize trends over time for total hires, average CTC, and relocation costs.
    * **Clustered Bar Charts:** For comparing metrics across regions, hiring modes, and age groups.
    * **Donut Charts:** To illustrate employee distribution by store size.
    * **Scatter Charts:** To explore correlations, e.g., `Hiring Cost` vs. `CTC`.
    * **Interactive Tables:** For detailed breakdowns of recent hires and relocated employees.
* **Interactivity & User Experience:**
    * **Slicers:** Dynamic slicers for filtering by `Region`, `Job Title`, `Hiring Mode`, `Year`, `Month`, `Home State`, and `Store Size`, enabling granular analysis.
    * **Dynamic Titles & Tooltips:** Enhanced user experience by providing context-sensitive information.
    * **Hidden Slicer Panels:** Implemented advanced bookmarking and button actions to create a clean, modern user interface with expandable slicer panels for improved dashboard aesthetics and usability.

---

## 🚀 How to Use the Dashboard

To explore this dashboard interactively:

1.  **Download the Power BI Desktop file:** Look for `Workforce_Hiring_Optimization_Dashboard.pbip` in this repository.
2.  **Open with Power BI Desktop:** Ensure you have Power BI Desktop installed on your machine.
3.  **Explore the Pages:** Navigate through the different tabs (Overview, Hiring Analysis, Employee Demographics, Store Staffing, Relocation Deep Dive) to uncover insights.
4.  **Utilize Slicers:** Use the interactive slicers on each page to filter data by region, job title, hiring mode, and time periods for customized views.
5.  **Hover for Details:** Hover over visuals to reveal detailed tooltips with specific data points.

---

## 🤝 Contribution & Support

Feedback and suggestions are always welcome!

* **Report Bugs:** If you encounter any issues, please open a [GitHub Issue](https://github.com/NelsonNeba/Furniture-Sales-Performance-Dashboard/issues).
* **Suggest Improvements:** Feel free to propose new features, metrics, or design enhancements via issues or by reaching out directly.

---

## 📜 License

This project is open-sourced under the MIT License. See the [LICENSE](LICENSE) file in the repository for full details.

---
