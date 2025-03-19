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

1. **Data Cleaning**: Load the dataset, handle missing values, and format key columns (`date_local`, `state_name`, `county_name`, `aqi`).  
2. **Descriptive Statistics**: Compute mean, median, standard deviation, and percentiles to summarize AQI trends.  
3. **Distribution Analysis**: Use log-transformed AQI values (`aqi_log`) to approximate normality, detect outliers via Z-scores.  
4. **Random Sampling**: Apply the Central Limit Theorem to estimate the population mean AQI from sample data.  
5. **Confidence Intervals**: Construct confidence intervals to quantify uncertainty in mean AQI estimates.  
6. **Hypothesis Testing**: Conduct t-tests to compare AQI across regions and evaluate policy impacts.  
7. **Visualization**: Use histograms, boxplots, and other charts to illustrate findings.

## Project Insights  

### **Descriptive Statistics**  
- **Mean AQI: 6.76**, indicating good air quality.  
- **75% of AQI values** are below **9**, suggesting most regions have satisfactory air quality.  
- **Max AQI: 50**, well below the unsafe threshold of 100.  

### **Distribution & Outliers**  
- **Log-transformed AQI** approximates normality for analysis.  
- **West Phoenix** is an outlier, requiring further investigation.  

### **Hypothesis Testing**  
- **Los Angeles vs. California**: No significant AQI difference.  
- **New York vs. Ohio**: New York has statistically lower AQI.  
- **Michigan**: AQI not significantly above 10, unlikely to be impacted by policy.  

### **Confidence Intervals**  
- **California’s 95% CI**: **[10.36, 13.88]**, suggesting potential policy impact.

## Project Highlights

- **Descriptive Statistics**: Summarized air quality data using mean, median, standard deviation, and percentiles.
- **Probability Distribution Modeling**: Used log-transformed AQI values to approximate a normal distribution and identify outliers.
- **Hypothesis Testing**: Conducted hypothesis tests to compare AQI values across regions and assess policy impacts.
- **Confidence Intervals**: Constructed confidence intervals to quantify uncertainty in mean AQI estimates.
- **Visualizations**: Created boxplots and histograms to visualize AQI trends and distributions.

## Future Work

- **Expand Analysis to Other Pollutants**: Investigate other AQI pollutants, such as nitrogen dioxide, sulfur dioxide, and ozone, to provide a more comprehensive understanding of air quality.
- **Develop Predictive Models**: Use historical AQI data to forecast future air quality trends and inform proactive policy decisions.
- **Conduct Region-Specific Studies**: Perform in-depth analyses of specific regions or states to identify localized challenges and opportunities.
- **Integrate with Socioeconomic Data**: Combine AQI data with socioeconomic indicators to better understand the factors influencing air quality.
- **Interactive Dashboards**: Create interactive dashboards using tools like Dash or Tableau to visualize air quality trends dynamically.

By building on the insights from this project, future research can advance our understanding of air quality trends, guiding environmental policies and public health strategies. This will contribute to cleaner air, reduced carbon monoxide pollution, and a healthier environment for all, ensuring sustainable development for future generations.
