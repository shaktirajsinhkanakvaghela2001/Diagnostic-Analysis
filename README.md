# Diagnostic-Analysis
# Diagnostic Analysis of Sales Decline at Walmart Retail

## Project Overview
This project investigates the root causes of sales fluctuations in Walmart retail stores using comprehensive data analysis. The analysis incorporates weekly sales data, economic indicators, and environmental factors to uncover patterns and correlations.

## Dataset
The analysis uses Walmart retail data containing:
- Store information
- Weekly sales figures (2011-2012)
- Holiday indicators
- Economic indicators (CPI, Unemployment Rate)
- Environmental factors (Temperature, Fuel Price)

## Key Findings

### 1. Sales Trend Analysis
The time series plot reveals:
- Significant seasonal fluctuations in weekly sales
- Highest sales during holiday periods (visible as spikes)
- Gradual decline in baseline sales from 2011 to 2012

### 2. Feature Importance (Random Forest)
![image](https://github.com/user-attachments/assets/9e32a55f-6b08-451e-bd84-ba49344c5f65)

The most influential factors on sales:
1. **Unemployment** (32% importance)
2. **CPI** (27% importance)
3. **Holiday_Flag** (2% importance)
4. **Temperature** (26% importance)
5. **Fuel_Price** (14% importance)

### 3. Regression Analysis Results
The OLS regression model (R² = 0.025) identified statistically significant relationships:

| Variable       | Coefficient | P-value | Impact Interpretation          |
|----------------|-------------|---------|---------------------------------|
| Unemployment   | -41,550     | 0.000   | Strong negative impact on sales |
| CPI            | -1,599      | 0.000   | Significant negative effect     |
| Holiday_Flag   | +74,890     | 0.007   | Positive holiday effect        |
| Temperature    | -724        | 0.071   | Marginal negative effect       |
| Fuel_Price     | -10,170     | 0.519   | Not statistically significant  |

**Key Insights:**
- Each 1% increase in unemployment correlates with $41,550 decrease in weekly sales
- Higher CPI (inflation) negatively impacts sales
- Holiday weeks generate $74,890 more in sales on average

## Recommendations

1. **Economic Sensitivity Planning**:
   - Develop targeted promotions during periods of high unemployment
   - Adjust inventory levels based on economic forecasts

2. **Pricing Strategy**:
   - Implement value-focused offerings during high inflation periods
   - Monitor CPI trends for pricing adjustments

3. **Seasonal Optimization**:
   - Maximize holiday promotions given their strong positive impact
   - Adjust staffing and inventory for temperature-sensitive products

4. **Further Research**:
   - Investigate additional factors beyond economic indicators
   - Conduct store-level analysis to identify high-performing locations

## Technologies Used
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook
- StatsModels (Regression Analysis)
- Scikit-learn (Random Forest)

## Limitations
- Moderate R² value (0.025) suggests other unmeasured factors influence sales
- Potential multicollinearity between economic indicators (CPI and Unemployment)
- Data limited to 2011-2012 period
