# EPA Carbon Monoxide AQI Analysis

This project analyzes air quality data from the Environmental Protection Agency (EPA), with a specific focus on carbon monoxide (CO) levels and their impact on air pollution and public health. Building on my previous analysis of the Air Quality Index (AQI), this study leverages Python libraries such as pandas, NumPy, SciPy, and Matplotlib to explore patterns, detect outliers, and conduct hypothesis testing. The goal is to provide data-driven insights to inform environmental policies, identify regions requiring intervention, and assess how air quality trends influence public health strategies.  

You can explore my earlier work on AQI analysis here:  
- [GitHub](https://github.com/Cyberoctane29/EPA-Air-Quality-AQI-Analysis): https://github.com/Cyberoctane29/EPA-Air-Quality-AQI-Analysis  
- [Kaggle](https://www.kaggle.com/code/saswatsethda/epa-air-quality-aqi-analysis): https://www.kaggle.com/code/saswatsethda/epa-air-quality-aqi-analysis

## Project Overview

The EPA Carbon Monoxide AQI Analysis project aims to:

- **Analyze air quality data** with a focus on carbon monoxide levels across various regions in the United States.
- **Perform descriptive statistics** to summarize air quality data and identify trends.
- **Determine probability distributions** to understand the spread of AQI values.
- **Detect outliers** using statistical techniques such as z-scores.
- **Apply sampling methods** to optimize analysis on large datasets.
- **Conduct hypothesis testing** to assess differences in AQI across locations.
- **Visualize key trends** in air pollution data to enhance interpretability.

The analysis is based on the following datasets:

1. **Dataset 1: c4_epa_air_quality.csv**  
   Contains raw air quality data, including carbon monoxide measurements, AQI values, and location details (state, county, city, and monitoring site).

2. **Dataset 2: modified_c4_epa_air_quality.csv**  
   Contains log-transformed AQI values (`aqi_log`) for improved statistical analysis.

## Dataset Structure

### Dataset 1: c4_epa_air_quality.csv
- **date_local**: The date of the air quality measurement.
- **state_name**: The U.S. state where the measurement was taken.
- **county_name**: The county where the monitoring site is located.
- **city_name**: The city where the measurement was recorded.
- **local_site_name**: The name of the specific monitoring station.
- **parameter_name**: The pollutant measured (carbon monoxide in this case).
- **units_of_measure**: The unit of measurement (parts per million).
- **arithmetic_mean**: The average concentration of carbon monoxide.
- **aqi**: The Air Quality Index (AQI) value derived from carbon monoxide levels.

### Dataset 2: modified_c4_epa_air_quality.csv
- **date_local, state_name, county_name, city_name, local_site_name, parameter_name, units_of_measure**: Same as Dataset 1.
- **aqi_log**: The natural logarithm of the AQI value for improved statistical analysis.

## Data Processing Steps

The data processing steps include:

1. **Loading and Cleaning Data**: The dataset is loaded into a pandas DataFrame, and missing values are handled to ensure data quality. Columns such as `date_local`, `state_name`, `county_name`, and `aqi` are cleaned and formatted for analysis.

2. **Descriptive Statistics**: Key statistics such as mean, median, standard deviation, and percentiles are computed to summarize the AQI data. This helps identify central tendencies and variability in air quality measurements.

3. **Probability Distribution Analysis**: The AQI data is analyzed using probability distributions, with log-transformed AQI values (`aqi_log`) used to approximate a normal distribution. Z-scores are calculated to detect outliers and assess data spread.

4. **Random Sampling**: Random samples are simulated to estimate the population mean AQI. The Central Limit Theorem is applied to validate the sampling distribution and ensure the sample mean approximates the population mean.

5. **Confidence Intervals**: Confidence intervals are constructed to quantify the uncertainty in the estimated mean AQI. This provides a range of values within which the true population mean is likely to fall.

6. **Hypothesis Testing**: Hypothesis tests are conducted to compare AQI values across different regions and assess policy impacts. For example:
   - A two-sample t-test compares the mean AQI of Los Angeles County to the rest of California.
   - A two-sample t-test compares the mean AQI of New York and Ohio.
   - A one-sample t-test evaluates whether Michigan’s mean AQI exceeds the policy threshold of 10.

7. **Visualization**: Data is visualized using histograms, boxplots, and other graphical tools to enhance interpretability and communicate findings effectively.

## Project Highlights

- **Descriptive Statistics**: Summarized air quality data using mean, median, standard deviation, and percentiles.
- **Probability Distribution Modeling**: Used log-transformed AQI values to approximate a normal distribution and identify outliers.
- **Hypothesis Testing**: Conducted hypothesis tests to compare AQI values across regions and assess policy impacts.
- **Confidence Intervals**: Constructed confidence intervals to quantify uncertainty in mean AQI estimates.
- **Visualizations**: Created boxplots and histograms to visualize AQI trends and distributions.

## Project Insights

### Descriptive Statistics
- The **mean AQI** across the dataset is **6.76**, indicating relatively good air quality.
- **75% of AQI values** are below **9**, suggesting that most regions have satisfactory air quality.
- The **maximum AQI value** is **50**, which is well below the threshold of 100, indicating safe air quality even in the worst cases.

### Probability Distribution Analysis
- The **log-transformed AQI data** (`aqi_log`) approximates a normal distribution, making it suitable for statistical analysis.
- **West Phoenix** was identified as an outlier with a significantly higher AQI value, suggesting the need for targeted interventions.

### Hypothesis Testing
- **Los Angeles County vs. Rest of California**: No statistically significant difference in AQI, indicating that air quality concerns are not uniquely concentrated in Los Angeles.
- **New York vs. Ohio**: New York has a statistically lower AQI than Ohio, making it a more suitable location for a regional office if air quality is a priority.
- **Michigan’s AQI**: Michigan’s mean AQI is not statistically greater than 10, suggesting it would not be affected by a new policy targeting states with higher AQI values.

### Confidence Intervals
- The **95% confidence interval** for California’s mean AQI is **[10.36, 13.88]**, indicating that California is likely to be impacted by the proposed policy.

## Future Work

- **Expand Analysis to Other Pollutants**: Investigate other AQI pollutants, such as nitrogen dioxide, sulfur dioxide, and ozone, to provide a more comprehensive understanding of air quality.
- **Develop Predictive Models**: Use historical AQI data to forecast future air quality trends and inform proactive policy decisions.
- **Conduct Region-Specific Studies**: Perform in-depth analyses of specific regions or states to identify localized challenges and opportunities.
- **Integrate with Socioeconomic Data**: Combine AQI data with socioeconomic indicators to better understand the factors influencing air quality.
- **Interactive Dashboards**: Create interactive dashboards using tools like Dash or Tableau to visualize air quality trends dynamically.

By building on the insights from this project, future research can advance our understanding of air quality trends, guiding environmental policies and public health strategies. This will contribute to cleaner air, reduced carbon monoxide pollution, and a healthier environment for all, ensuring sustainable development for future generations.
