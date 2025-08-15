# PowerBI Practical Exam

## Project Overview
This repository contains the complete PowerBI practical exam project analyzing AdventureWorks Sales Data. The project demonstrates proficiency in data import, transformation, modeling, visualization creation, report building, dashboard design, and advanced features including DAX calculations and Row-Level Security.

## Approach and Methodology

### Data Import and Transformation
- Connected to AdventureWorks Excel file with 7 core tables
- Implemented comprehensive data cleaning in Power Query Editor
- Created calculated columns for Profit analysis and Sales Categories
- Applied data quality filters (removed pre-2018 records)
- Handled missing values and removed duplicates

### Data Modeling
- Built robust star schema with Sales as central fact table
- Created relationships between all dimension tables (Customer, Product, Date, etc.)
- Developed hierarchical structures for Date (Year > Quarter > Month > Day) and Product (Category > Subcategory > Product)
- Optimized model by hiding surrogate keys and formatting measures appropriately

### Visualization and Reporting
- Created 4 comprehensive report pages with 20+ interactive visuals
- Implemented cross-filtering and drill-down capabilities across all charts
- Applied consistent themes and color schemes for accessibility
- Built responsive dashboard with mobile optimization
- Utilized advanced visuals including custom bullet charts, treemaps, and multi-row cards
- Integrated running totals and performance tracking metrics

## Screenshots

### Star Schema
![Star Schema](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/main/Screenshots/MODELVIEW.png?raw=true)
*Star schema showing relationships between fact and dimension tables*

### Report Pages

#### Sales Overview
![Sales Overview](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/main/Screenshots/SALES%20OVERVIEW.png?raw=true)
*Comprehensive sales dashboard featuring:*
- KPI cards with sales targets and running totals
- Sales trend line chart with forecasting
- Geographic map with drill-down capabilities
- Sales distribution donut chart by category
- Multi-row cards displaying key performance metrics
- Interactive slicers for Year, Category, and Region

#### Product Analysis
![Product Analysis](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/main/Screenshots/PRODUCT_ANALYSIS.png?raw=true)
*Product performance analysis including:*
- Profit analysis donut chart by product
- Treemap visualization of sales amount by category
- Interactive product comparisons and rankings
- Category performance breakdowns

#### Customer Insights
![Customer Insights](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/main/Screenshots/CUSTOMER_INSIGHTS.png?raw=true)
*Customer behavior and segmentation analysis with:*
- Key customer metrics cards (Country count, Total Sales)
- Multi-row card featuring profit margin, budget, total sales, total customers, and top customer sales
- Custom bullet chart for performance vs targets
- Sales distribution donut chart by category
- Customer performance analysis

#### Visuals Gallery
![Visuals Gallery](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/main/Screenshots/VISUALS_GALLERY.png?raw=true)
*Showcase of advanced visualization techniques*

#### Dashboard
![Dashboard](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/main/Screenshots/DASHBOARD.png?raw=true)
*Dashboard showcase*

### Row-Level Security
![RLS Setup](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/d75dd62a732ece134887c7bf89870d2618e41a84/Screenshots/ROLES.png)
*Security role configuration for data access control*

![RLS Testing](https://github.com/QazGeo/PowerBI_Practical_Exam_George/blob/d75dd62a732ece134887c7bf89870d2618e41a84/Screenshots/ROLE_TEST.png)
*Testing results showing filtered data by role*

## Key Insights

### Sales Performance
- **Total Revenue**: $97 million across all periods
- **Peak Performance**: The month of May showed highest sales volume
- **Geographic Distribution**: USA had the most sales overall

### Product Analysis
- **Top Category**: Bikes contributed 96% of total sales
- **Best Performing Product**: Touring-3000 Yellow, 62 with $351,000 revenue
- **Profit Margins**: Average margin of 11% with Bike category showing highest profitability

### Customer Behavior
- **Geographic Concentration**: Most customers are from the United States
- **Purchase Patterns**: Bikes are purchased way higher than all products in all regions

### Forecasting
- **6-Month Projection**: Expected revenue of $206 million based on trend analysis
- **Growth Trajectory**: An upward trend anticipated

## Row-Level Security Implementation
- **US Manager Role**: Access restricted to United States data only
- **Europe Manager Role**: Access to UK, Germany, France, and Australia data
- **Testing**: Successfully validated role-based data filtering in PowerBI Service
- **Security Model**: Applied at Customer/Territory level with country-based filters

## Challenges Faced and Solutions

### Challenge 1: Date Table Complexity
**Issue**: Multiple date-related tables after transformations
**Solution**: Maintained both original Date table (for relationships) and Date Summary table (for aggregations)

### Challenge 2: Relationship Ambiguity
**Issue**: Multiple potential relationship paths between tables
**Solution**: Carefully designed star schema with Sales as central fact table, ensuring single active relationships

### Challenge 3: DAX Performance
**Issue**: Complex calculations affecting report performance
**Solution**: Optimized DAX formulas using CALCULATE and proper filter contexts

### Challenge 4: RLS Testing
**Issue**: Difficulty testing security roles during development
**Solution**: Used PowerBI Service testing features and documented results with screenshots

## Assumptions and Limitations

### Assumptions
- **Data Quality**: Assumed source data accuracy after basic cleaning
- **Currency**: All monetary values assumed to be in USD
- **Forecast Model**: Linear trend assumption for 6-month projection
- **Geographic Data**: Country classifications based on available dataset values
- **Business Rules**: Standard fiscal year calendar assumed
- **Customer Segmentation**: Arbitrary thresholds used for High/Medium/Low categorization

### Limitations
- **Real-time Data**: Analysis based on historical data only, no real-time updates
- **External Factors**: Does not account for external market conditions, seasonality beyond historical patterns
- **Data Scope**: Limited to AdventureWorks sample data, may not reflect real-world complexity
- **Security Model**: Simplified RLS implementation, enterprise scenarios may require more granular control
- **Forecast Accuracy**: Linear projection may not account for business cycles or market changes
- **Geographic Granularity**: Limited to country/region level, city-level analysis constrained by data availability
- **Product Lifecycle**: Does not account for product launch dates or discontinuation
- **Currency Fluctuations**: Single currency assumption may not reflect multi-national operations
