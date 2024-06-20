## Project Description

This project analyzes the earnings quality signals of various companies by calculating accrual components, standardizing them, and forming long/short portfolios based on these accruals. The project utilizes financial statement data from 2020 and 2021 and company stock returns to compute size-adjusted cumulative abnormal returns.

### Methodology

1. **Data Loading and Preparation:**
   - The financial data for 2020 and 2021 is loaded and filtered to include only those companies with available data for both years.
   - Duplicate entries are removed to ensure data integrity.

2. **Accrual Component Calculation:**
   - Changes (deltas) in various financial statement components such as Current Assets, Cash, Current Liabilities, etc., are calculated.
   - The Accrual Component is computed using the formula: 
     \[
     \text{Accrual Component} = (\Delta CA - \Delta Cash) - (\Delta CL - \Delta STD - \Delta TP) - Dep
     \]
   - The Cash Component is also calculated to understand the non-accrual part of earnings.

3. **Standardization of Accrual Component:**
   - The Accrual Component is standardized by dividing it by the average total assets of the companies.

4. **Size-Adjusted Cumulative Abnormal Returns:**
   - Company stock returns and size-matched stock returns are loaded and merged.
   - Cumulative returns for individual and size-matched returns are calculated for the period from May 2022 to April 2023.
   - Size-adjusted abnormal returns are computed as the difference between cumulative individual returns and size-matched returns.

5. **Forming Long/Short Portfolio:**
   - Companies are sorted based on their Per Asset Accruals.
   - The top 25 companies with the lowest Per Asset Accruals form the Long Portfolio.
   - The top 25 companies with the highest Per Asset Accruals form the Short Portfolio.
   - Average Per Asset Accrual and Average Size-Adjusted Cumulative Abnormal Returns are calculated for both portfolios.

### Insights and Conclusion

- **Average Per Asset Accrual for Long Portfolio:** -0.5511
- **Average Per Asset Accrual for Short Portfolio:** 0.7991
- **Average Size-Adjusted Cumulative Abnormal Returns for Long Portfolio:** -0.0326
- **Average Size-Adjusted Cumulative Abnormal Returns for Short Portfolio:** -0.1634
- **Hedge Return:** 0.1307

The analysis indicates that companies with lower Per Asset Accruals (Long Portfolio) generally have better performance in terms of size-adjusted cumulative abnormal returns compared to those with higher Per Asset Accruals (Short Portfolio). This finding suggests that lower accruals may signal higher earnings quality and better stock performance.

### Visualizations

#### Descriptive Statistics
![Descriptive Statistics](images/descriptive_statistics_screenshot.png)

#### Long Portfolio Statistics
![Long Portfolio Statistics](images/long_portfolio_statistics_screenshot.png)

#### Short Portfolio Statistics
![Short Portfolio Statistics](images/short_portfolio_statistics_screenshot.png)

### Companies in Long and Short Portfolios

#### Long Portfolio
![Long Portfolio](images/long_portfolio_screenshot.png)

#### Short Portfolio
![Short Portfolio](images/short_portfolio_screenshot.png)

### Graphs

#### Histogram of Per Asset Accruals for Long and Short Portfolios
![Histogram](images/histogram_screenshot.png)

#### Boxplot of Size-Adjusted Cumulative Abnormal Returns for Long and Short Portfolios
![Boxplot](images/boxplot_screenshot.png)

#### Scatter Plot of Per Asset Accrual vs. Size-Adjusted Cumulative Abnormal Returns
![Scatter Plot](images/scatter_plot_screenshot.png)


### Additional Project Description

The project is based on the earnings quality signal developed by Richard Sloan, a former accounting professor at the University of Michigan. This signal allows one to compare earnings quality across companies using the accrual metric.

#### Data Sources
- **Financial Statement Data:** Extracted from the Compustat database.
- **Stock Returns Data:** Obtained from the CRSP database.
- **Size-Matched Stock Returns:** Provided in the project data.

#### Preface
The project follows the methodology of Barclays Global Investors (BGI) in creating long/short stock portfolios designed to generate excess or abnormal (alpha) returns using signals like the earnings quality signal.

This project provides valuable insights into the relationship between accrual components and stock performance, aiding in investment decisions based on earnings quality signals.
