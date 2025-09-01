#  Maven Market Analytics Dashboard (Power BI)

##  Project Overview  
This project is an interactive **Power BI dashboard** built for Maven Market, a retail analytics simulation focused on brand-level sales, profit margin analysis, and return performance. The report visualizes **key business metrics**, integrates **geographic filters**, and leverages data from various interrelated tables to support strategic decision-making.

---

##  Objectives  
- Track and visualize **monthly sales performance**, profit, and returns against dynamic goals.  
- Analyze product-level profitability and return rates across multiple brands.  
- Monitor regional performance with interactive map visuals.  
- Provide users with **drillable views**, slicers, and geographic breakdowns to explore insights by country and store.  
- Summarize insights using **bookmark-driven performance notes**.

---

##  Data Source & Schema  
The model consists of several normalized tables connected via Power BI’s relationship view. These tables support slicing by time, geography, product, and store.

| Table Name         | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `Transactions Data` | Contains metrics like Total Revenue, Total Profit, Total Transactions, and YTD Revenue. |
| `Returns Data`      | Tracks return quantity, total returns, and return rates at product and store levels. |
| `Products`          | Product-level details including brand, cost, price tier, and category.     |
| `Customers`         | Demographic metadata (e.g., location, age, gender) supporting deeper insights. |
| `Calendar`          | Time dimension used for monthly, weekly, and quarterly analysis.           |
| `Stores`            | Store-level metadata: location, size, region, remodeling date, etc.        |
| `Regions`           | Regional-level mappings and sales districts.                              |

 Relationships are primarily **1:many** between lookup tables (e.g., Calendar, Products) and fact tables (Transactions, Returns).

![Model View](images/Model%20View.JPG)

---

##  Dashboard Features

###  KPIs (Top Row Cards)
- **Current Month Transactions**: Total transactions this month vs. goal.
- **Current Month Profit**: Profit value compared to goal.
- **Current Month Returns**: Number of product returns this month vs. target.

Each card dynamically reflects performance using green/red arrows and percentage comparisons.

###  Brand-Level Profitability Table
A matrix-style visual displays key metrics by product brand:
- **Total Transactions**
- **Total Profit**
- **Profit Margin %** (with green gradient for higher margins)
- **Return Rate %** (with red gradient for higher return rates)

 *Conditional formatting helps quickly spot underperforming or high-return brands.*

![Topline Performance Dashboard](images/Topline%20Performance%20Dashboard.JPG)


###  Interactive Map (Geo Analysis)
- Bubble map showing **total transaction volume** by store location.
- Filter buttons: **USA**, **Mexico**, **Canada**, and **Select All**.
- Country-based comparisons shown via color-coded bar/treemap visuals.

![Maven Market GIF 1](images/Maven%20Market.%20GIF%201.gif)
![Canada Filtered](images/Canada%20Filtered.JPG)

###  Weekly Revenue Trend (Time Series)
- Column chart showing weekly revenue patterns over time.
- Helps track seasonality and spikes in revenue across different months.

###  Revenue vs. Target (Gauge)
- Radial visual showing **progress toward monthly or yearly revenue targets**.
- Dynamically updates with filters and country selections.

---

##  Key Insights

As displayed in the **Performance Notes** visual section:
-  **Plato** products achieved the **highest overall profit margin (63.55%)** in 1998.
-  **Bravo** had the **lowest number of transactions** during the same period.
-  **Portland** store reached a milestone of **1,000 sales in December**, indicating strong local engagement.

These notes are designed to **summarize user-relevant performance highlights** in natural language.

![Maven Market GIF 2](images/Maven%20Market.GIF%202.gif)
![Plato products drove the strongest overall profit margin (63.55%) in 1998](images/Plato%20products%20drove%20the%20strongest%20overall%20profit%20margin%20%2863.55%25%29%20in%201998.JPG)
![Bravo products sales have the Lowest transactions in 1998](images/Bravo%20products%20sales%20have%20the%20Lowest%20transactions%20in%201998.JPG)
![Portland reached 1,000 sales in December to close out the year](images/Portland%20reached%201%2C000%20sales%20in%20December%20to%20close%20out%20the%20year.JPG)

---

##  Tools & Techniques

| Tool / Feature        | Purpose                                                              |
|-----------------------|----------------------------------------------------------------------|
| **Power BI Desktop**  | Report authoring and modeling environment                            |
| **Power Query Editor**| Cleaning, shaping, and integrating data sources                      |
| **Data Modeling**     | Building star schema with relationships across fact and dimension tables |
| **DAX Measures**      | Custom calculations (e.g., Profit Margin, Return Rate, Goal Variance)|
| **Conditional Formatting** | Visual cues to highlight performance variances                     |
| **Bookmarks & Tooltips** | Used for drillable insights and narrative storytelling                |

---

##  Visual Interaction Features
- **Slicers** for geography-based filtering (country or store-level)
- **Hover tooltips** on KPIs and charts for extra context
- **Bookmark-driven narrative cards** to highlight notable achievements

---

##  Learning Outcomes
- Created an **executive-ready dashboard** with clean layout and branded visuals.
- Applied **advanced DAX** to calculate custom KPIs and goal tracking.
- Demonstrated proficiency in **Power BI modeling**, **geo-mapping**, and **user-driven analytics**.
- Built visuals supporting both **high-level summaries** and **deep dives** into brand/store performance.

---

##  Conclusion  
The **Maven Market Dashboard** presents a compelling example of retail-focused analytics using Power BI. From dynamic KPI tracking to deep brand and store insights, it offers a comprehensive view into sales and operational performance—ready for presentation to stakeholders or executive users.