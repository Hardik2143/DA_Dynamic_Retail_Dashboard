## Dynamic Retail Dashboard in Excel

### Overview
The Dynamic Retail Dashboard is an interactive, data-driven solution developed in Excel to provide insights into retail performance. Leveraging datasets hosted on GitHub, Power Query for data transformation, and dynamic visualizations, it addresses key business questions, enabling strategic decision-making through actionable insights.

### Datasets Used

#### 1. **Orders Table**
Details customer orders, including product, shipping, and financial metrics.

**Sample Data:**

| Order ID         | Returned | Order Date | Ship Date | Ship Mode    | Customer Name | Segment   | Country       | Market | Sales   | Profit  | Discount |
|------------------|----------|------------|-----------|--------------|----------------|-----------|---------------|--------|---------|---------|----------|
| CA-2012-124891  | No       | 31-07-2020 | 31-07-2020| Same Day     | Rick Hansen   | Consumer  | United States | US     | 2309.65 | 762.18  | 0        |
| IN-2013-77878   | Yes      | 05-02-2021 | 07-02-2021| Second Class | Justin Ritter | Corporate | Australia     | APAC   | 3709.40 | -288.77 | 0.1      |
| IN-2013-71249   | No       | 17-10-2021 | 18-10-2021| First Class  | Craig Reiter  | Consumer  | Australia     | APAC   | 5175.17 | 919.97  | 0.1      |

#### 2. **Returns Table**
Tracks returned orders and their respective markets.

**Sample Data:**

| Returned | Order ID       | Market        |
|----------|----------------|---------------|
| Yes      | MX-2013-168137 | LATAM         |
| Yes      | US-2011-165316 | LATAM         |
| Yes      | ES-2013-1525878| EU            |
| Yes      | CA-2013-118311 | United States |

#### 3. **People Table**
Contains information about sales representatives and their regions.

**Sample Data:**

| Person            | Region    |
|-------------------|-----------|
| Anna Andreadi     | Central   |
| Chuck Magee       | South     |
| Kelly Williams    | East      |
| Matt Collister    | West      |
| Deborah Brumfield | Africa    |

### Problem Statements Solved with Steps

#### 1. **Key Performance Indicators (KPIs)**
**Objective:** Dynamically calculate and display Total Sales, Total Profit, Total Quantity, Number of Orders, and Profit Margin.

**Steps:**
- Use Power Query to import the Orders Table.
- Create calculated columns for:
  - Profit Margin = Profit / Sales.
  - Total Orders = COUNT(Order ID).
- Use Excel formulas to calculate:
  - Total Sales = SUM(Sales).
  - Total Profit = SUM(Profit).
  - Total Quantity = SUM(Quantity).
- Design a dynamic KPI table with symbols for visual enhancement (e.g., 💰 for Total Sales).

---

#### 2. **Sales and Profit Analysis**
**Objective:** Visualize sales and profit trends to identify patterns.

**Steps:**
- Create a Pivot Table with Order Date grouped by Year and Month.
- Add Sales and Profit as values.
- Develop a Line Chart to showcase trends.
- Add slicers to filter by category, market, or region.

---

#### 3. **Category-Wise Profit**
**Objective:** Analyze profitability across categories.

**Steps:**
- Create a Pivot Table using Category as rows and Profit as values.
- Sort in descending order by Profit.
- Create a Bar Chart to visualize category profitability.
- Integrate slicers for interactivity.

---

#### 4. **Segment-Wise Sales Share (%)**
**Objective:** Show sales proportion by customer segment.

**Steps:**
- Create a Pivot Table with Segment as rows and Sales as values.
- Calculate percentage share using = Sales / Total Sales * 100.
- Develop a Pie or Donut Chart to display sales share.
- Add dynamic labels showing percentage values.

---

#### 5. **Sales by Country**
**Objective:** Analyze sales performance geographically.

**Steps:**
- Create a Pivot Table with Country as rows and Sales as values.
- Sort in descending order of Sales.
- Apply conditional formatting or use a Geographic Map Chart.

---

#### 6. **Top 5 Subcategories**
**Objective:** Identify top-performing subcategories.

**Steps:**
- Create a Pivot Table with Sub-Category as rows and Sales as values.
- Sort in descending order of Sales.
- Filter for the top 5 Sub-Categories.
- Use a Column Chart to visualize results.

---

#### 7. **Bottom 5 Subcategories**
**Objective:** Highlight underperforming subcategories.

**Steps:**
- Use the same Pivot Table as above but sort in ascending order of Sales.
- Filter for the bottom 5 Sub-Categories.
- Use a contrasting Column Chart for visualization.

---

#### 8. **Yearly Sales Trends**
**Objective:** Analyze sales trends over multiple years.

**Steps:**
- Create a Pivot Table with Order Date grouped by Year.
- Add Sales as values.
- Develop a Line Chart to display the trend.
- Include slicers for filtering by category, region, or segment.

### Dynamic Features
- **Dynamic Charts:** Automatically update based on slicer inputs.
- **Power Query Integration:** Streamlines data cleaning and transformation.
- **KPI Table:** Highlights essential metrics at a glance.

### Next Steps for Extension
Enhance the dashboard with additional insights:
- **Return Analysis:** Examine return rates by market or product category.
- **Top and Bottom Customers:** Identify the most and least profitable customers.
- **Market Analysis:** Compare performance across different markets.
- **Product Analysis:** Evaluate contributions of individual products.

### Significance
This dashboard enables retail businesses to:
- Monitor performance using KPIs.
- Analyze trends across categories, segments, and regions.
- Make informed, data-driven decisions.

### Visuals
The repository includes:
- Sample visuals for each problem statement.
- Final dashboard snapshots showcasing all components dynamically.

